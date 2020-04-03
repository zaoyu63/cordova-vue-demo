# cordova-vue-demo
基于 vue、cordova搭建的跨平台移动端基础工程

## 主要技术
 + 前端框架 <a href="https://cn.vuejs.org">Vue</a>
 + 跨平台框架 <a href="http://cordova.axuer.com/">Cordova</a>
 + 插件 <a href="http://www.ionic.wang/native_doc-index.html">Ionic Native</a>
 
## 效果图
![demo](./demo.png)

## 主要功能   
 + h5端工程
 + 生成android工程，支持生成apk文件 
 + 生成ios工程，可以通过xcode进行模拟
 
## 使用教程

 1. 安装 nodejs, 网上找教程安装
 2. 安装 cordova
 ```$xslt
sudo npm install -g cordova
```
 3. 下载项目 
 ```$xslt
 git clone https://github.com/zaoyu63/cordova-vue-demo.git
 cd cordova-vue-demo
 npm install
```
 4. web端本地开发
 浏览器输入http://localhost:8006/#/ 进行访问
 ```$xslt
npm run dev
```
 5. 生成android项目
 ```$xslt
npm run android
// 生成的项目在platform下
```
6. 生成ios项目
```$xslt
npm run ios
```
## 插件使用
参照 <a href="http://cordova.axuer.com/">Cordova</a>、<a href="http://www.ionic.wang/native_doc-index.html">Ionic Native</a> 文档

## android 环境配置 
以mac系统为例

1.安装 android-sdk
   可以选择安装<a href="http://www.android-studio.org/">Android Studio</a>，或者仅安装 命令行工具 <a href="https://dl-ssl.google.com/android/repository/sdk-tools-darwin-4333796.zip">SDK tools package</a>，本文采用命令行工具安装
```
  cd
  mkdir android-sdk
  把下载的命令行工具压缩包解压到android-sdk、  android-sdk目录下有一个tools目录
  cd android-sdk/android-sdk/bin
   安装 platform-tools 和 build-tools
  ./sdkmanager "platform-tools" "platforms;android-28"
  ./sdkmanager "build-tools;28.0.0"
```
2.安装Gradle
```$xslt
brew install gradle
```
3.配置环境变量  
```$xslt
cd
vi .bashrc
// 在.bashrc增加下面几行配置
export PATH="/Users/tw/android-sdk/platform-tools:/Users/tw/android-sdk/tools"
export JVAV_HOME=/usr/bin/java
export ANDROID_HOME=/Users/tw/andriod-sdk
source .bashrc
```
3.测试配置环境是否正常
```$xslt
cordova requirements

Requirements check results for android:
Java JDK: installed 1.8.0
Android SDK: installed true
Android target: installed android-28
Gradle: installed /usr/local/Cellar/gradle/6.3/bin/gradle

Requirements check results for ios:
Apple macOS: installed darwin
Xcode: installed 11.1
ios-deploy: not installed 
ios-deploy was not found. Please download, build and install version 1.9.2 or greater from https://github.com/ios-control/ios-deploy into your path, or do 'npm install -g ios-deploy'
CocoaPods: installed 1.9.1
Some of requirements check failed

andriod 和 ios 环境都是正常的，如果出现错误，检查环境变量是否正常
```

## 打包andriod成apk安装包
```
npm run ba
```
