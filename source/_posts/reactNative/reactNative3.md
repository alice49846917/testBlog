---
title: react-native开发总结——常用插件
date: 2020-07-21 07:07:41
tags: 
  - react-native
type: hexo                                                                         # 标签、分类和友情链接三個页面需要配置(必填)
description: 快速、简洁且高效的博客框架                                                            # 描述
keywords: react-navive插件                                                                       # 关键词，便于搜索
top_img: /images/reactNative/images/logo.jpg             # 文章的顶部图片
aside: true                                                                         # 展示文章侧边栏(默认为true)
categories: 
  - 教程
  - react-native 
cover: /images/reactNative/images/logo.jpg                 # 文章的缩略图（用在首页）
---

# 多环境配置react-native-config
  * 详细文档请看: https://github.com/luggit/react-native-config

  * 下载安装包:   当前版本("react-native-config": "^1.3.1")
    ```
      yarn add react-native-config
    ```
  
  * 连接库: (react-native 0.60版本后可以不执行这个命令)
    ```
      npx react-native link react-native-config
    ```

  * ios端需要连接库:
    ```
      在当前项目下进入ios目录, 执行:
      pod install
    ```

  * android端链接库:
    1. 在当前项目下的android/settings.gradle添加：
    ```
      include ':react-native-config'

      project(':react-native-config').projectDir = new File(rootProject.projectDir, '../node_modules/react-native-config/android') 
    ```

    2. 将插件添加到android/app/build.gradle中：
      ```
        apply from: project(':react-native-config').projectDir.getPath() + "/dotenv.gradle"
      ```

  * 基本使用
    1. 在项目根路径下新建.env.development和.env.production文件,写点内容(文件名一定要.env开头，否则没有效果)
      ```
        API_URL=https://myapi.com
        GOOGLE_MAPS_API_KEY=abcdefgh
      ```
    
    2. 在package.json中，添加命令:
      ```
        "dev": "SET ENVFILE=.env.development && react-native run-android",
        "prod": "SET ENVFILE=.env.production && react-native run-android"
      ```

    3. 在js项目中使用该配置：
      ```
        import Config from "react-native-config";

        console.log(Config.API_URL); // 'https://myapi.com'
      ```

    4. 在android工程中使用多环境:
      ```
        # 进入到andorid目录，执行: 
        ENVFILE=.env.development ./gradlew assembleRelease
      ```

    5. 在ios工程中使用多环境: 
      ```
        The basic idea in iOS is to have one scheme per environment file, so you can easily alternate between them.

        Start by creating a new scheme:

        In the Xcode menu, go to Product > Scheme > Edit Scheme
        Click Duplicate Scheme on the bottom
        Give it a proper name on the top left. For instance: "Myapp (staging)"
        Then edit the newly created scheme to make it use a different env file. From the same "manage scheme" window:

        Expand the "Build" settings on left
        Click "Pre-actions", and under the plus sign select "New Run Script Action"
        Where it says "Type a script or drag a script file", type:

        cp ${PROJECT_DIR}/../.env.staging .env  # replace .env.staging for your file
      ```
***

# 项目绝对路径babel-plugin-module-resolver
  * 为了防止引入时不断的../，使用babel-plugin-module-resolver

  * 下载安装包: 
    ```
      yarn add babel-plugin-module-resolver
    ```

  * 在babel.config.js中改造并添加: 
    ```
      plugins: [
        [
          'module-resolver',
          {
            root: ['./src'],
            alias: {
              '@/utils': './src/utils',
              '@/pages': './src/pages',
              '@/components': './src/components',
              '@/models': './src/models',
              '@/assets': './src/assets'
            }
          }
        ]
      ]
    ```

  * 在tsconfig.json中修改配置：
    ```
      "baseUrl": "./src",                         
      "paths": {
        "@/assets/*": ["assets/*"],
        "@/components/*": ["components/*"],
        "@/models/*": ["models/*"],
        "@/pages/*": ["pages/*"],
        "@/utils/*": ["utils/*"],
      },
    ```
    
  * 使用方式和vue完全一样，以根路径为@
    ```
      import App from '@/src/pages/Home/Main'
    ```

***

# 导航器react-navigation（5.x）
  1. 安装核心包：
    ```
      yarn add @react-navigation/native
    ```

  2. 安装相应的依赖包：
    ```
      yarn add react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context @react-native-community/masked-view
    ```

  3. 在根路径的index.js中引入react-native-gesture-handler，否则生产环境会报错

  4. 在你应用的根路径Home/index.tsx中，使用NavigationContainer进行包裹：
    ```
      import 'react-native-gesture-handler';
      import {AppRegistry} from 'react-native';
      import App from '@/src/pages/Home';
      import {name as appName} from './app.json';
      import { NavigationContainer } from '@react-navigation/native';

      AppRegistry.registerComponent(appName, () => <NavigationContainer><App /></NavigationContainer>);
    ```

## 堆栈式导航器
  1. 详细文档请看: https://reactnavigation.org/docs/stack-navigator

  2. 安装核心包：
    ```
      yarn add @react-navigation/stack
    ```

  3. 创建堆栈式导航器   
      * createStackNavigator标签包含两个子组件Screen和Navigator
      ```
        import React, { Component } from 'react'
        import { NavigationContainer } from '@react-navigation/native'
        import { createStackNavigator } from '@react-navigation/stack'
        import Home from '@/pages/Home'
        import Detail from '@/pages/Home/Detail'

        type RootStackList = { // 定义类型别名
          Home: undefined,
          Detail: undefined
        }

        let Stack = createStackNavigator<RootStackList>()

        export default class Navigator extends Component {
          render() {
            return (
              <NavigationContainer>
                <Stack.Navigator>
                  <Stack.Screen
                    options={{
                      headerTitleAlign: 'center',
                      headerTitle: '首页'
                    }}
                    name="Home"
                    component={Home}
                  />
                  <Stack.Screen 
                    name="Detail" 
                    component={Detail}
                    options={{
                      headerTitleAlign: 'center',
                      headerTitle: '详情页首页'
                    }}
                  />
                </Stack.Navigator>
              </NavigationContainer>
            )
          }
        }
      ```

      * Stack.Navigator可以接收screenOptions属性，用于配置所有的导航器的样式

  4. 页面传参：
    * home页面跳转到detail页面
    ```
      # home页面传递：
        this.props.navigation.navigate('Detail', {id: '123'})

      # detail页面接收
        <Text> {this.props.route.params.id} </Text>
    ```

  5. 详细代码请看
    * router/index.tsx里： 
      ```
        import React, { Component } from 'react'
        import { NavigationContainer } from '@react-navigation/native'
        import { createStackNavigator, StackNavigationProp, HeaderStyleInterpolators, CardStyleInterpolators } from '@react-navigation/stack'
        import Home from '@/pages/Home'
        import Detail from '@/pages/Home/Detail'

        export type RootStackList = { // 定义类型别名，用于约束navigator组件，在添加组件时，这里必须声明类型
          Home: undefined,
          Detail: {
            id: string
          }
        }

        // 该类型申明约束每一个页面组件的props
        export type RootStackNavigation = StackNavigationProp<RootStackList>

        let Stack = createStackNavigator<RootStackList>()

        export default class Navigator extends Component {
          render() {
            return (
              <NavigationContainer>
                <Stack.Navigator
                  headerMode='screen'
                  screenOptions={{
                    headerTitleAlign: 'center', // 标题内容居中
                    // 下面两句是统一ios和安卓的页面切换效果
                    headerStyleInterpolator: HeaderStyleInterpolators.forUIKit,
                    cardStyleInterpolator: CardStyleInterpolators.forHorizontalIOS,
                    // 开启安卓的切换手势
                    gestureEnabled: true,
                    gestureDirection: 'horizontal'
                  }}
                >
                  <Stack.Screen
                    options={{
                      headerTitle: '首页'
                    }}
                    name="Home"
                    component={Home}
                  />
                  <Stack.Screen 
                    name="Detail" 
                    component={Detail}
                    options={{
                      headerTitle: '详情页'
                    }}
                  />
                </Stack.Navigator>
              </NavigationContainer>
            )
          }
        }
      ```

      * Home.tsx里：
        ```
          import React, { Component } from 'react'
          import { Text, View, Button } from 'react-native'
          import { RootStackNavigation } from '@/router/index'

          interface homeProps {
            navigation: RootStackNavigation
          }

          export default class Home extends Component<homeProps> {
            render() {
              return (
                <View>
                  <Text> textInComponent </Text>
                  <Button title='跳转到详情页面' onPress={()=>{
                    this.props.navigation.navigate('Detail', {id: '123'})
                  }} />
                </View>
              )
            }
          }
        ```

      * Detail.tsx里：
        ```
          import React, { Component } from 'react'
          import { Text, View } from 'react-native'
          import { RootStackList } from '@/router/index'
          import { RouteProp } from '@react-navigation/native'

          interface Iprops{
            route: RouteProp<RootStackList, 'Detail'>
          }

          export default class Detail extends Component<Iprops> {
            render() {
              console.log(this.props)
              return (
                <View>
                  <Text> {this.props.route.params.id} </Text>
                </View>
              )
            }
          }
        ```
  
{% note warning %}
注意：   
  * 设置标题位置为居中还是居左：Stack.Navigator组件的screenOptions属性
    ```
      <Stack.Navigator
        screenOptions={{
          headerTitleAlign: 'center', // 标题内容居中
        }}
      ></Stack.Navigator>
    ```

  * 设置页面切换的动画效果（统一ios）：Stack.Navigator组件的headerStyleInterpolator和cardStyleInterpolator属性
    ```
      <Stack.Navigator
        screenOptions={{
          // 设置页面切换的风格
          headerStyleInterpolator: HeaderStyleInterpolators.forUIKit, // 头部统一
          cardStyleInterpolator: CardStyleInterpolators.forHorizontalIOS // 页面主体内容统一
        }}
      >
    ```

  * 隐藏导航栏：Stack.Navigator组件的headerMode属性
    ```
      <Stack.Navigator
        headerMode='node'
      >
    ```

  * 开启安卓的切换手势(默认是关闭的)：Stack.Navigator组件的screenOptions属性
      ```
        <Stack.Navigator
          screenOptions={{
            // 开启安卓的切换手势
            gestureEnabled: true,
            gestureDirection: 'horizontal'
          }}
        >
      ```
{% endnote %}

## 底部导航栏
  1. 安装核心包：
    ```
      yarn add @react-navigation/bottom-tabs
    ```

  2. 创建底部导航器
    * createBottomTabNavigator标签包含两个子组件Screen和Navigator
      ```
        import React, { Component } from 'react'
        import { NavigationContainer } from '@react-navigation/native'
        import { createBottomTabNavigator } from '@react-navigation/bottom-tabs'
        import Home from '@/pages/Home'
        import Account from '@/pages/Account'
        import Found from '@/pages/Found'
        import Listen from '@/pages/Listen'

        export type BottomTabParamList = {
          Home: undefined,
          Found: undefined,
          Listen: undefined,
          Account: undefined
        }

        const Tab = createBottomTabNavigator<BottomTabParamList>()


        export default class BottomTabs extends Component {
          render() {
            return (
              <NavigationContainer>
                <Tab.Navigator tabBarOptions={{
                  activeTintColor: '#c71622'
                }}>
                  <Tab.Screen name='Home' component={Home} options={{ tabBarLabel: '首页' }}></Tab.Screen>
                  <Tab.Screen name='Listen' component={Listen} options={{ tabBarLabel: '我听' }}></Tab.Screen>
                  <Tab.Screen name='Found' component={Found} options={{ tabBarLabel: '发现' }}></Tab.Screen>
                  <Tab.Screen name='Account' component={Account} options={{ tabBarLabel: '用户' }}></Tab.Screen>
                </Tab.Navigator>
              </NavigationContainer>
            )
          }
        }

        # 最后在根路径引入即可
      ```

  3. 堆栈导航器嵌套底部导航栏
    * 在router/index.tsx里：
      ```
        import React, { Component } from 'react'
        import { NavigationContainer } from '@react-navigation/native'
        import { createStackNavigator, StackNavigationProp, HeaderStyleInterpolators, CardStyleInterpolators } from '@react-navigation/stack'
        import Detail from '@/pages/Home/Detail'
        import BottomTabs from '@/router/BottomTabs'

        export type RootStackList = { // 定义类型别名，用于约束navigator组件，在添加组件时，这里必须声明类型
          Tab: {
            screen?: string
          },
          Detail: {
            id: string
          }
        }

        // 该类型申明约束每一个页面组件的props
        export type RootStackNavigation = StackNavigationProp<RootStackList>

        let Stack = createStackNavigator<RootStackList>()

        export default class Navigator extends Component {
          render() {
            return (
              <NavigationContainer>
                <Stack.Navigator
                  headerMode='screen'
                  screenOptions={{
                    headerTitleAlign: 'center', // 标题内容居中
                    // 下面两句是统一ios和安卓的页面切换效果
                    headerStyleInterpolator: HeaderStyleInterpolators.forUIKit,
                    cardStyleInterpolator: CardStyleInterpolators.forHorizontalIOS,
                    // 开启安卓的切换手势
                    gestureEnabled: true,
                    gestureDirection: 'horizontal'
                  }}
                >
                  <Stack.Screen
                    name="Tab"
                    component={BottomTabs}
                  />
                  <Stack.Screen 
                    name="Detail" 
                    component={Detail}
                    options={{
                      headerTitle: '详情'
                    }}
                  />
                </Stack.Navigator>
              </NavigationContainer>
            )
          }
        }
      ```

    * 在router/BottomTabs.tsx里：
      ```
        import React, { Component } from 'react'
        import { NavigationContainer } from '@react-navigation/native'
        import { createStackNavigator, StackNavigationProp, HeaderStyleInterpolators, CardStyleInterpolators } from '@react-navigation/stack'
        import Detail from '@/pages/Home/Detail'
        import BottomTabs from '@/router/BottomTabs'

        export type RootStackList = { // 定义类型别名，用于约束navigator组件，在添加组件时，这里必须声明类型
          Tab: {
            screen?: string
          },
          Detail: {
            id: string
          }
        }

        // 该类型申明约束每一个页面组件的props
        export type RootStackNavigation = StackNavigationProp<RootStackList>

        let Stack = createStackNavigator<RootStackList>()

        export default class Navigator extends Component {
          render() {
            return (
              <NavigationContainer>
                <Stack.Navigator
                  headerMode='screen'
                  screenOptions={{
                    headerTitleAlign: 'center', // 标题内容居中
                    // 下面两句是统一ios和安卓的页面切换效果
                    headerStyleInterpolator: HeaderStyleInterpolators.forUIKit,
                    cardStyleInterpolator: CardStyleInterpolators.forHorizontalIOS,
                    // 开启安卓的切换手势
                    gestureEnabled: true,
                    gestureDirection: 'horizontal'
                  }}
                >
                  <Stack.Screen
                    name="Tab"
                    component={BottomTabs}
                  />
                  <Stack.Screen 
                    name="Detail" 
                    component={Detail}
                    options={{
                      headerTitle: '详情'
                    }}
                  />
                </Stack.Navigator>
              </NavigationContainer>
            )
          }
        }
      ```

    * 在根路径的index.js中，引入Navigator即可

***

# 时间选择组件：rmc-date-picker

## 安装：
  ```
    npm install --save rmc-date-picker
  ```

## 使用：
  ```
    import DatePicker from 'rmc-date-picker'

    <DatePicker
      defaultDate={moment(new Date()).toDate()}
      locale={lang}
      mode={props.modeType}
      maxDate={moment().add(30, 'y').toDate()}
      minDate={moment([1980, 1, 1, 1, 1, 1]).toDate()}
      onDateChange={(v) => {
        console.log('v', v)
      }}
    />
  ```

## 详细文档:
  https://www.npmjs.com/package/rmc-date-picker

***

# 下拉选择组件：Picker

## 安装：
  ```
    npm install --save @react-native-community/picker

    ios一定要进入ios文件夹，执行pod install
  ```

## 使用：
  ```
    import {Picker} from '@react-native-community/picker';

    <Picker
      selectedValue={this.state.language}
      style={{height: 50, width: 100}}
      onValueChange={(itemValue, itemIndex) =>
        console.log(itemValue, itemIndex)
        this.setState({language: itemValue})
      }>
      <Picker.Item label="Java" value="java" />
      <Picker.Item label="JavaScript" value="js" />
    </Picker>
  ```
***

# 文字提示组件: react-native-root-toast
## 下载核心包:
  ```
    yarn add react-native-root-toast 或者 npm install --save react-native-root-toast
  ```

## 当react-native的版本>0.62时，需要在根路径src/index.tsx或者App.tsx中，加入以下代码：
  ```
    import { RootSiblingParent } from 'react-native-root-siblings';

    return (
      <RootSiblingParent>  // <- use RootSiblingParent to wrap your root component
        <App />
      </RootSiblingParent>
    );
  ```

## 具体使用:
  ```
    import Toast from 'react-native-root-toast';

    Toast.show('This is a message', {
      duration: Toast.durations.LONG,
      position: Toast.positions.BOTTOM,
      shadow: true,
      animation: true,
      hideOnPress: true,
      delay: 0,
    });
  ```

## 详细说明文档
  详细说明文档请看：https://github.com/magicismight/react-native-root-toast

## 详细文档：
  https://www.npmjs.com/package/@react-native-community/picker

***

# 弹窗组件:react-native-modalbox
## 下载核心包:
  ```
    npm install react-native-modalbox@latest --save
    npm install --save-dev @types/react-native-modalbox
  ```

## 使用:
  ```
      import Modal from 'react-native-modalbox'

      <Modal
        isOpen={this.state.visible}
        style={{height: UnitConvert.dpi(300)}}
        position='top'
        startOpen
        onClosed={()=>{
          this.setState({
            visible: false
          })
        }}
      >
        <Text>2222</Text>
      </Modal>
  ```

## 详细文档:
  https://github.com/maxs15/react-native-modalbox#readme

***

# 缓存组件: async-storage
## 下载核心包:
  ```
    npm install -- save @react-native-community/async-storage
  ```
## 封装及使用：
  ```
    import AsyncStorage from "@react-native-community/async-storage";

    export default class Storage {
      // 获取key的值
      static async get(key: string) {
        return AsyncStorage.getItem(key)
      }

      // 设置Key的值
      static async set(key: string, value: any) {
        return AsyncStorage.setItem(key, value)
      }

      // 删除Key的值
      static async delete(key: string) {
        return AsyncStorage.removeItem(key)
      }

      // 删除所有的值
      static async deleteAll() {
        return AsyncStorage.clear()
      }
    }

    调用：
      设置值: 
        Storage.set('user', '张三')

      获取值: 
        Storage.get('user').then(res=>{
          console.log(res)
        })
      
      删除值:
        Storage.remove('user')
  ```

## 详细文档请看：https://github.com/react-native-async-storage/async-storage

***

# 图片选择组件(可多选): react-native-image-crop-picker
## 下载核心包：
    ```
      npm install --save react-native-image-crop-picker

      注意：低版本的sdk，不识别标签导致项目跑不起来，我选的是0.30.0的版本，最新的0.35.1有问题
    ```

## 使用：
      ```
        # 在android\app\src\main\AndroidManifest.xml添加相机权限

          <!-- 获取拍照权限 -->
          <uses-permission android:name="android.permission.CAMERA" />


        使用：
          import ImagePicker from 'react-native-image-crop-picker';

          ImagePicker.openPicker({
            width: 300,
            height: 400,
            cropping: true
          }).then(image => {
            console.log(image);
          });
      ```

## 详细文档：
https://github.com/ivpusic/react-native-image-crop-picker