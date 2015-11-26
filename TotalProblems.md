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
[ibireme的各种iOS资源收藏夹](http://github.ibireme.com/github/list/ios/#)

20151124
-------------
#### GCD的blog
学习GCD的原理以及源代码，[深入理解GCD -- CocoaChina](http://www.cocoachina.com/ios/20151117/14225.html)

#### Page Container Controller
[做页面切换的Page Controller](https://github.com/wangmchn/WMPageController)

20151125
---------------
#### Image Handle Technology
1. [iOS保持页面流畅的技巧](http://blog.ibireme.com/2015/11/12/smooth_user_interfaces_for_ios/#more-41893)
2. [AsyncDisplayKit](https://github.com/facebook/AsyncDisplayKit)
3. What is Bitmap?
4. What is Thread Safety?
5. [缓存TableViewCell的高度--百度开源的Example](https://github.com/forkingdog/UITableView-FDTemplateLayoutCell/)

#### 提供两个参考链接
* cnblog[位图和矢量图的区别](http://www.cnblogs.com/areliang/archive/2006/04/29/388769.html)
* 歪果的网站[Difference between bitmap and vector](http://etc.usf.edu/techease/win/images/what-is-the-difference-between-bitmap-and-vector-images/)


20151126
------------
#### 插件管理器Alcatraz
* [Alcatarz github地址](https://github.com/alcatraz/Alcatraz)
* [唐巧的博客介绍](http://blog.devtang.com/blog/2014/03/05/use-alcatraz-to-manage-xcode-plugins/)
