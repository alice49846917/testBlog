---
title: react-native开发总结
date: 2020-06-26 09:59:45
tags: 
  - react-native
  - 适配
type: hexo                                                                         # 标签、分类和友情链接三個页面需要配置(必填)
description: 快速、简洁且高效的博客框架                                                            # 描述
keywords: hexo的搭建                                                                       # 关键词，便于搜索
top_img: /images/reactNative/images/logo.jpg             # 文章的顶部图片
aside: true                                                                         # 展示文章侧边栏(默认为true)
categories: 
  - 教程
  - react-native                                                                 # 文章标签
  - 适配
cover: /images/reactNative/images/logo.jpg                 # 文章的缩略图（用在首页）
---

# 开发环境的搭建
## 下载jdk
  * 下载地址: https://www.oracle.com/java/technologies/javase-downloads.html
  * ![jdk的安装与配置](/images/reactNative/images/jdk安装及配置.jpg)
  {% note primary %}
    注意：推荐下载jdk1.8及以上的版本，下载之后配置环境变量
  {% endnote %}

## 下载android studo
  * 下载地址: https://developer.android.google.cn/studio/
  {% note primary %}
    android studo推荐使用3.5以上的版本，然后下载android sdk，选择8.1以上的版本
  {% endnote %}
  * ![android studio和android sdk下载安装](/images/reactNative/images/androidstudio环境搭建.jpg)
  * ![安卓环境变量](/images/reactNative/images/android环境变量.jpg)
  
## 创建react-native项目
  * 输入命令：npx react-native init myproject

***

# 分辨率的适配， Dimensions
  * 详细代码如下：
  ```
      import { Dimensions, View } from 'react-native'

      // 适配方案
      export const sumPx = {
        dpi: (w) => { // 自适应px, 750为设计稿的宽度
          return width / 750 * w
        },
        h: height,
        w: width
      }

      使用方法
      <View style={{width: sumPx.dpi(300), height: sumPx.dpi(300), backgroundColor: 'red'}}></View>
  ```
  * [详细代码请看:https://github.com/dj49846917/react-native-study/blob/master/docs/example/%E9%80%82%E9%85%8D/UnitConvert.js](https://github.com/dj49846917/react-native-study/blob/master/docs/example/%E9%80%82%E9%85%8D/UnitConvert.js)

# 代码调试
  * 输入命令： adb shell input keyevent 82， 唤起调试菜单
    
  * 唤起之后，选择debug，会弹出谷歌浏览器，然后console里面就能打印你代码中的console.log
    ![代码调试](/images/reactNative/images/代码调试.jpg)
    
  * 取消debug只需要再次唤起菜单，点击stop
    ![取消代码调试](/images/reactNative/images/取消代码调试.jpg)

# 获取导航栏的高度
  * 要先下载react-navigation

```
  import { Header } from 'react-navigation';

  const navHeight = Header.HEIGHT;
  console.log(navHeight)
```

# react-navigation重置路由(5.x版本)
  1. 需求：app第一次进来先判断是否登录，如果没有登录，就跳转到登录页面，登录了就跳转到首页，但是返回的时候，登录和启动页都不要显示
  
  2. 实现方法：
    ```
      使用CommonActions的reset方法重置路由

      import { useNavigation, CommonActions } from '@react-navigation/native';

      navigation.dispatch(
        CommonActions.reset({
          index: 1,
          routes: [
            { name: 'Login' },
          ],
        })
      );
    ```  
