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

#### 提供bitmap相关的两个参考链接
* cnblog -- [位图和矢量图的区别](http://www.cnblogs.com/areliang/archive/2006/04/29/388769.html)
* 歪果的网站 -- [Difference between bitmap and vector](http://etc.usf.edu/techease/win/images/what-is-the-difference-between-bitmap-and-vector-images/)


20151126
------------
#### 插件管理器Alcatraz
* [Alcatarz github地址](https://github.com/alcatraz/Alcatraz)
* [唐巧的博客介绍](http://blog.devtang.com/blog/2014/03/05/use-alcatraz-to-manage-xcode-plugins/)

#### 正则表达式RegexKitLite
* 官方文档 -- [RegexKitLite Document](http://regexkit.sourceforge.net/RegexKitLite/)
* github地址 -- [RegexKitLite Repo](https://github.com/wezm/RegexKitLite)
* cnblog博客解释 -- [iOS中使用RegexKitLite来试用正则表达式](http://blog.csdn.net/luckilyyu/article/details/6229048)
* 芳仔小脚印的OSC-Blog -- [分分钟学会正则表达式](http://my.oschina.net/joanfen/blog/415076?fromerr=YekKe49J)

20151127
-----------
#### 线程安全Thread Safety
* stackoverflow -- [Aotomic properties vs Thread Safety](http://stackoverflow.com/questions/21098494/atomic-properties-vs-thread-safe-in-objective-c)
* Learn is Tasty -- [iOS Multithreading: Thread Safety in iOS Applications](http://sodecon.blogspot.com/2012/08/ios-multithreading-thread-safety-in-ios.html)
* stackoverflow -- [Does @synchronized guarantees thread safety or not](http://stackoverflow.com/questions/15392726/does-synchronized-guarantees-for-thread-safety-or-not)

20151130
--------------
#### XMPP and Socket
* Quora -- [How does XMPP differ from socket])https://www.quora.com/How-does-XMPP-differ-from-Sockets-Why-is-it-good-to-implement-XMPP-instead-of-Sockets-while-implementing-some-IM-based-app-What-options-as-an-Android-developer-do-we-have-besides-XMPP-if-we-want-to-build-an-IM-app)
* stackoverflow -- [iOS difference between socket and XMPP](http://stackoverflow.com/questions/7430567/difference-between-socket-connection-and-xmpp-connection)
* apple document -- [iOS socket programming guide](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/NetworkingTopics/Articles/UsingSocketsandSocketStreams.html)

#### new library manager for iOS
* www.isaced.com -- [Cocoa 新的依赖管理工具：Carthage](http://www.isaced.com/post-265.html)
* CocoaChina -- [Carthage：去中心化的Cocoa依赖管理器](http://www.cocoachina.com/ios/20141204/10528.html)

#### Network Problems
* www.webopedia.com -- [Difference between ipv4 and ipv6](http://www.webopedia.com/DidYouKnow/Internet/ipv6_ipv4_difference.html)
* stackoverflow -- [Difference between tcp and udp](http://stackoverflow.com/questions/5970383/difference-between-tcp-and-udp)
