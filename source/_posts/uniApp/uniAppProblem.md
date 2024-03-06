---
title: uni-app问题收集及解决
date: 2020-11-26 14:38:48
tags: 
  - uni-app
type: uni-app                                                                 # 标签、分类
description:  是一个使用 Vue.js 开发所有前端应用的框架，开发者编写一套代码，可发布到iOS、Android、Web（响应式）、以及各种小程序（微信/支付宝/百度/头条/QQ/钉钉/淘宝）、快应用等多个平台。
top_img: /images/uniApp/logo.jpg             # 文章的顶部图片
aside: true                                                                         # 展示文章侧边栏(默认为true)
categories: 
  - 教程
  - uni-app                                                                 # 文章标签
cover: /images/uniApp/logo.jpg                 # 文章的缩略图（用在首页）
---

# css部分
## nvue支持sass但是不支持sass的嵌套
  * 变量使用(**支持**)
    ```
      <style lang="scss">
        $lineBorderColor: yellow;
        .icon_right{
          font-size: 50px;
          color: $lineBorderColor;
        }
      </style>
    ```

  * 外部scss文件引入(**支持**)
    ```
      <style lang="scss">
        @import "../../constant/css/constant.scss";
        .icon_right{
          font-size: 50px;
          color: $lineBorderColor;
        }
      </style>
    ```

  * nvue不支持sass嵌套
  
  * nvue支持sass的所有其他属性，举例mixin(混合)
    ```
      // constant.scss文件

      $lineBorderColor: #dfdfdf;
      @mixin my {
        justify-content: center;
        align-items: center;
        height: 200rpx;
        border-color: red;
        border-width: 2px;
        border-style: solid;
        width: 750rpx;
        background-color: pink;
      }

      // home.nvue中

      <style lang="scss">
        @import "../../constant/css/constant.scss";
        .icon_right{
          font-size: 50px;
          color: $lineBorderColor;
        }
        .list {
          @include my;
        }
      </style>
    ```

***

## 在nvue中，绑定style计算值的时候一定要放在computed里，放在生命周期里没有效果
  * 举例：动态设置状态栏的高度
      ```
        <view class="tipBar" :style="getStatusBarHeight"></view>

        computed: {	
          getStatusBarHeight() {
            // #ifdef APP-PLUS-NVUE
            return `height: ${plus.navigator.getStatusbarHeight()}px`
            // #endif
          }
        },
      ```

***

## 不可用css收集
### display
  * 在nvue中，默认就是display: flex,所以在nvue中，不支持display属性，写了在app端不支持，其他端可以
  * display: none不能使用，要想隐藏dom只能用v-if

### border
  * 在vue中，border的3个属性需要分开写，不能像vue那样
  * 举例：
    ```
      # 在vue中：
        border: 1px solid #ccc;

      # 在nvue中:
        border-color: #ccc;
        border-width: 1px;
        border-style: solid;
    ```

### max-,min-系列
  * 在app端，nvue不支持
  * 其他端支持

## uni-app中，解决iconfont图标 unicode转换为字符串
  * 举例：
    * iconfont图标: `&#xe649;`
    * 转成字符串是: \ue649

## 在uni-app中，使用scroll-view组件，动态获取滚动高度
  * 小程序端：屏幕高度 - 状态栏 - 导航栏 - 底部导航栏(有的情况下)
  * 其他端: 屏幕高度 - 状态栏 - 导航栏
  * 详细代码:
      ```
        computed: {
          ...mapState({
            // 获取状态栏的高度
            getStatusBarHeight: (state) => {
              return `height: ${state.app.tipBarHeight}px`
            },
            // 获取可滚动区域的高度
            getScrollHeight: (state)=>{
              const navBarHeight = uni.upx2px(90)
              const tabBarHeight = uni.upx2px(110)
              // #ifndef MP
              const scrollHeight = state.app.height - state.app.tipBarHeight - navBarHeight - tabBarHeight;
              return `height: ${scrollHeight}px`;
              // #endif
              
              // #ifdef MP
              const scrollHeight2 = state.app.height - state.app.tipBarHeight - navBarHeight;
              return `height: ${scrollHeight2}px`;
              // #endif
            }
          }),
        },
      ```

## nvue布局bug：定位问题
  1. app端：
    * ![布局bug](/images/uniApp/布局bug_app端.jpg)
  
  2. 小程序端和h5端:
    * ![布局bug](/images/uniApp/布局bug_h5和小程序端.jpg)

  3. bug布局代码:
      ```
      <view class="list">
        <view class="list_left_box">
          <image src="@/static/images/userpic.jpg" class="list_icon"></image>
          <view class="list_left_tip">
            <text class="list_left_tip_num">2</text>
          </view>
        </view>
      </view>

      # style部分
        .list {
          width: 750rpx;
          height: 135rpx;
          flex-direction: row;
          align-items: center;
        }
        .list_left_box {
          width: 92rpx;
          height: 92rpx;
          margin-left: 30rpx;
          margin-right: 20rpx;
        }
        .list_left_tip {
          padding: 0 10rpx;
          border-radius: 18rpx;
          background-color: red;
          position: absolute;
          right: -16rpx;
          top: -16rpx;
          @include center;
        }
        .list_icon {
          width: 92rpx;
          height: 92rpx;
          border-radius: 10rpx;
        }
        .list_left_tip_num {
          font-size: 26rpx;
          color: #fff;
        }
      ```

  4. 分析原因：在app端，由于图标盒子的宽高只有92rpx，60rpx的margin, 而整个list的高度是135rpx
   
  5. 解决方法: 布局不变，将盒子的宽度设成92+60, 高度=list的高度
      ```
        <view class="list">
          <view class="list_left_box">
            <image src="@/static/images/userpic.jpg" class="list_icon"></image>
            <view class="list_left_tip">
              <text class="list_left_tip_num">2</text>
            </view>
          </view>
        </view>

        # style部分

        .list {
          width: 750rpx;
          height: 135rpx;
          flex-direction: row;
          align-items: center;
        }
        .list_left_box {
          width: 152rpx;
          height: 135rpx;
          padding: 0 30rpx;
          padding-top: 21.5rpx;
        }
        .list_left_tip {
          padding: 0 10rpx;
          border-radius: 18rpx;
          background-color: red;
          position: absolute;
          right: 16rpx;
          top: 10rpx;
          @include center;
        }
        .list_icon {
          width: 92rpx;
          height: 92rpx;
          border-radius: 10rpx;
        }
        .list_left_tip_num {
          font-size: 26rpx;
          color: #fff;
        }
      ```

## 在uni-app中，要在模板中给函数传值，要写成箭头函数，不然在小程序中获取不到值
  * 错误写法：
    ```
      <view class="alphabet" :style="getAlphabetPos">
        <view class="alphabet_item" v-for="(piece, index) in chatList" :key="piece.id" @click="handleAlphabet(piece)">
          <text class="alphabet_item_text">{{ piece.title }}</text>
        </view>
      </view>
    ```

  * 正确写法：
    ```
      <view class="alphabet" :style="getAlphabetPos">
        <view class="alphabet_item" v-for="(piece, index) in chatList" :key="piece.id" @click="()=>handleAlphabet(piece)">
          <text class="alphabet_item_text">{{ piece.title }}</text>
        </view>
      </view>
    ```

## 在uni-app中，解决输入框输入内容整体上移的问题
  * 设置input的adjust-position=false即可

## 在uni-app中，在scroll-view中，直接绑定click事件在app端是没有效果的，只能在他里面再建一个view绑定事件，在scoll-view外面绑定也不行
  ```
    <scroll-view scroll-y="true" :style="getScrollHeight">
			<view :style="getScrollHeight" @click="closeKeyBoard">
				<view class="chat_item">
					<chat-item-list></chat-item-list>
				</view>
			</view>
		</scroll-view>
  ```

## uni-app中，button组件，三端的兼容性很差，布局用view+text代替

## uni-app中，主动弹出键盘，或者在初始化的时候自动弹出键盘
  * 解决办法，设置input的focus属性即可
## uni-app中，使用uni.getSystemInfoSync()获取高度的时候，小程序不算tabbar的高度
  * 举例：如果你是在有tabbar的时候算的屏幕高度，那么在跳转进没有tabbar的高度的时候，一定要使用uni.getSystemInfoSync()重新算一次，不要将就之前算的

## 在uni-app中，使用template或者block做循环的时候，不能把key绑定在上面
  ```
    <view class="menu_list">
      <template v-for="item in list">
        <view v-if="item.id < 8" class="menu_list_item1" :key="item.id">
          <view class="menu_list_item_box">
            <text class="iconfont menu_list_item_box_icon">{{ item.icon }}</text>
          </view>
          <text class="menu_list_item_text">{{ item.text }}</text>
        </view>
      </template>
    </view>
  ```

## 将scroll-view组件初始化在最底部的方法:
  * 使用scroll-view的scroll-into-view属性，给循环体一个id
  * 通过计算获取循环体的length -1赋值即可
    ```
      <scroll-view scroll-y="true" :style="getScrollStyle" :scroll-into-view="scrollIntoView">
        <view @click="closeKeyBoard">
          <view class="chat_item" v-for="(item, index) in list" :key="index" :id="'chatItem_'+index">
            <chat-item-list ref="list"></chat-item-list>
          </view>
        </view>
      </scroll-view>


      // 回到底部
			pageToBottom(){
				this.$nextTick(function(){
					let lastIndex = this.list.length - 1
					this.scrollIntoView = 'chatItem_'+lastIndex
				})
			},
    ```


## 在nvue中，app端不支持gif图
  * 解决办法: 利用定时器做动态的图片切换模拟gif
    ```
      <image :src="now" mode="" class="model_content_icon"></image>

      export default {
        data() {
          return {
            timer: null,
            pic: ["/static/images/audio1.png", "/static/images/audio2.png", "/static/images/audio3.png"],
            i: 0,
            now: "/static/images/audio1.png",
            timer: null
          }
        },
        mounted: function() {
          this.now = this.pic[0];
          let _this = this;
          clearInterval(this.timer)
          this.timer = setInterval(function() {
            _this.i++;
            _this.now = _this.pic[_this.i];
            if (_this.i >= _this.pic.length - 1) {
              _this.i = -1;
            }
            console.log("_this.now", _this.now)
          }, 600)
        },
        beforeDestroy() {
          clearInterval(this.timer);
          this.timer = null;
        },
      }
    ```

## uni-app中，app端使用uni.getRecorderManager()获取不到录音的时长，在小程序端可以，H5用不了这个组件，只能用第三方插件
  * 解决办法:
    * app端: 利用按下和收起两个事件去计算之间的时间差
      ```
        data() {
          return {
            pressStartTime: 0,	// 按下的时间
            pressEndTime: 0,	// 松开的时间
            audioObj: null,		// 录音的对象
          };
        },

        methods: {
          // touchstart语音
          audioStart() {
            console.log('11')
            this.pressStartTime = 0
            this.pressStartTime = new Date().valueOf()
            // #ifndef H5
              this.audioObj = uni.getRecorderManager();
              this.audioObj.start();
            // #endif
          },
          
          // touchend语音
          audioEnd() {
            // #ifndef H5
            console.log("this.audioObj", this.audioObj)
            this.pressEndTime = new Date().valueOf()
            const duration = this.pressEndTime - this.pressStartTime - 50
            this.audioObj.stop()
            this.audioObj.onStop((res)=>{
              console.log("res", res)
              // #ifdef MP
                const params = {
                  
                }
              // #endif
            })
            // #endif
            this.pressEndTime = 0
            this.audioObj = null
          },
        }
      ```

    * 小程序端使用uni.getRecorderManager()的onStop方法获取得到音频的时长