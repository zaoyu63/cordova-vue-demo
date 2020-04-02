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

 1. 安装 nodejs, 网站找教程安装
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

1. 安装 android-sdk
   可以选择安装<a href="http://www.android-studio.org/">Android Studio</a>，或者仅安装 命令行工具 <a href="https://dl-ssl.google.com/android/repository/sdk-tools-darwin-4333796.zip">SDK tools package</a>
   


