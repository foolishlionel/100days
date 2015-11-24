20151122
-------------
#### 安装CocoaPods出现的问题
##### 首先要更新到较高的ruby版本
rvm reinstall ruby-2.0.0-p247 --with-gcc=clang --verify-downloads 1 [参考链接 stackoverflow](http://stackoverflow.com/questions/20790994/cocoapods-failing-to-install-with-xcode-5-0-2)
##### 使用淘宝的ruby源（镜像源？）
$ gem sources --remove https://rubygems.org/

$ gem sources --remove http://ruby.taobao.org/

$ gem sources -a https://ruby.taobao.org/
> 注意：命令行结尾的`/`不要丢失。

##### 查看当前的ruby资源
$ gem sources -l

此处我们需要的ruby镜像源是"https://ruby.taobao.org/"

##### 接着安装cocoapods
sudo gem isntall cocoapods

##### Pod setup without sudo
pod setup

##### pod install without sudo
pod install


在此过程中可能会出现安装失败的情况，主要是Permission Denied，参考[Permission Denied Stackoverflow](http://stackoverflow.com/questions/16049335/cocoapods-pod-install-permission-denied)

#### Chrome浏览器的Dolphin爬墙插件
* [Dolphin官方下载地址](https://glbproxy.com/html/ec/index.html)


20151123
--------------
#### 定义常用的Block
* typedef void (^requestSuccessBlock)(id responseObj);
* typedef void (^requestFailedBlock)(NSError *error);
* typedef void (^responseBlock)(id dataObj, NSError *error);
* typedef void (^progressBlock)(int64_t bytesWritten, int64_t totalBytesWritten， int64_t totalBytesExpectedToWrite);
[参考链接CocoaChina](http://www.cocoachina.com/ios/20151123/14344.html)

#### 资源收藏
[某某某的收藏夹](http://github.ibireme.com/github/list/ios/#)

20151124
-------------
#### GCD的blog
学习GCD的原理以及源代码，[深入理解GCD -- CocoaChina](http://www.cocoachina.com/ios/20151117/14225.html)

#### Page Container Controller
[做页面切换的Page Controller](https://github.com/wangmchn/WMPageController)
