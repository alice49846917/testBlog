---
title: react native日常开发遇到的问题
date: 2020-10-09 09:18:25
tags: 
  - react-native
  - 开发问题及解决办法
type: hexo                                                                         # 标签、分类和友情链接三個页面需要配置(必填)
description: 快速、简洁且高效的博客框架                                               # 描述
keywords: react-navigation,navigationOptions无法获取到this                          # 关键词，便于搜索
top_img: /images/reactNative/images/logo.jpg             # 文章的顶部图片
aside: true                                                                         # 展示文章侧边栏(默认为true)
categories: 
  - 教程
  - react-native 
cover: /images/reactNative/images/logo.jpg                 # 文章的缩略图（用在首页）
---

# react-native navigationOptions中不能获取this、state
## 场景：在createStackNavigator路由过来的页面，navigationOptions的header中添加搜索框
  * 如下图：![如下图](/images/reactNative/images/problem/001.png)

    ```
      static navigationOptions = {
        headerStyle: {backgroundColor: '#0086f1'},
        headerTitle: (
            <TextInput placeholder={'请输入搜索内容'}
                       onChangeText={(text) => this.setState({'str': text})
      };
      constructor(props) {
          super(props)；
          this.state = ({
              str: ''
          })
      };
    ```

  * 使用this.setState的时候出现如下错误: ![错误](/images/reactNative/images/problem/002.png)
  {% note default %}
    因为this对象为null，所以找不到setState方法
  {% endnote %}

## 解决办法：外部引用
  * 在最外部申明：
    ```
      let that;
    ```

  * 在class内部赋值
    ```
      constructor(props){
        super(props);
        that = this;
      }
    ```

  * 完整代码:
    ```
      let that;//外部申明
      export default class MinePage extends Component<Props> {

          static navigationOptions = {
            ......
          };

          constructor(props) {
              super(props);
              that=this;
              this.state = ({
                  str: ''
              })
          };
          
          render() {
              return (
                  <View style={styles.container}>
                      //使用外部申明变量
                      <Text>{that.state.str}</Text>
                  </View>
              );
          }
      }
    ```

  {% note primary %}
    参考：https://www.cnblogs.com/yuxingxingstar/p/9804170.html
    https://blog.csdn.net/qq_35324309/article/details/88848315
  {% endnote %}

***

# textInput在android中，如果字体大小太小，垂直方向无法居中
##  解决办法：在textInput中的设置padding: 0

# react-native 在ios中，图片不显示的问题
## 解决办法：
  * 在node_modules/react-native/Libraries/RCTUIImageViewAnimated.m中273行修改以下代码：
    ```
      # 修改前：
      - (void)displayLayer:(CALayer *)layer
      {
        if (_currentFrame) {
          layer.contentsScale = self.animatedImageScale;
          layer.contents = (__bridge id)_currentFrame.CGImage;
        }
      }

      # 修改后：
      - (void)displayLayer:(CALayer *)layer
      {
        if (_currentFrame) {
          layer.contentsScale = self.animatedImageScale;
          layer.contents = (__bridge id)_currentFrame.CGImage;
        } else {
          [super displayLayer:layer];
        }
      }
    ```

  * [详细解决方案](https://www.jianshu.com/p/97c89d566ae4)

  