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
* Quora -- [How does XMPP differ from socket](https://www.quora.com/How-does-XMPP-differ-from-Sockets-Why-is-it-good-to-implement-XMPP-instead-of-Sockets-while-implementing-some-IM-based-app-What-options-as-an-Android-developer-do-we-have-besides-XMPP-if-we-want-to-build-an-IM-app)
* stackoverflow -- [iOS difference between socket and XMPP](http://stackoverflow.com/questions/7430567/difference-between-socket-connection-and-xmpp-connection)
* apple document -- [iOS socket programming guide](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/NetworkingTopics/Articles/UsingSocketsandSocketStreams.html)

#### new library manager for iOS
* isaced -- [Cocoa 新的依赖管理工具：Carthage](http://www.isaced.com/post-265.html)
* CocoaChina -- [Carthage：去中心化的Cocoa依赖管理器](http://www.cocoachina.com/ios/20141204/10528.html)

#### Network Problems
* webopedia -- [Difference between ipv4 and ipv6](http://www.webopedia.com/DidYouKnow/Internet/ipv6_ipv4_difference.html)
* stackoverflow -- [Difference between tcp and udp](http://stackoverflow.com/questions/5970383/difference-between-tcp-and-udp)

20151201
-----------
#### Usage of CocoaPods
* csdn -- [iOS开发~CocoaPods使用详细说明](http://blog.csdn.net/showhilllee/article/details/38398119) 解释：之前在自己的电脑上面安装，出现各种问题，导致自己觉得pods使用未免太过繁琐，后来在公司使用Pods，参照本篇教程，一次就安装成功了，我的内心真的是有点崩溃啊。

#### NSRecursiveLock
* CocoaChina -- [NSRecursiveLock递归锁的使用](http://www.cocoachina.com/ios/20150513/11808.html) NSRecursiveLock实际上定义的是一个递归锁，这个锁可以被同一线程多次请求而不会引起死锁。这主要用在循环或递归操作中。
* Sina Blog -- [几种不同的锁](http://blog.sina.com.cn/s/blog_8c87ba3b0101ok8y.html)

#### NSCoding,NSSecureCoding以及NSCopying协议
* Apple Document -- [NSCoding Protocol Reference](https://developer.apple.com/library/prerelease/ios/documentation/Cocoa/Reference/Foundation/Protocols/NSCoding_Protocol/index.html)
* Apple Document -- [Encoding and Decoding Objects](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/Archiving/Articles/codingobjects.html)
* blog.jobbole.com -- [使用NSSecureCoding协议进行对象编解码](http://blog.jobbole.com/67655/)

#### Runloop的切换

#### NSURLCredential身份认证

20151203
---------------
#### dispatch_queue_t
* cnblog -- [iOS多线程的初步研究](http://www.cnblogs.com/sunfrog/p/3305614.html)

#### dispatch_group_t
* commandshift -- [Using dispatch groups](http://commandshift.co.uk/blog/2014/03/19/using-dispatch-groups-to-wait-for-multiple-web-services/)
* cnblog -- [dispatch_group_t](http://www.cnblogs.com/chinaxxren/p/3457814.html)

20151204
-------------
* cocoachina -- [iOS 事件处理机制与图像渲染过程](http://www.cocoachina.com/ios/20151203/14549.html)


20151209
-------------
* WX_cocoachina -- [利用OC的消息转发机制实现多重代理](http://mp.weixin.qq.com/s?__biz=MjM5OTM0MzIwMQ==&mid=401491246&idx=2&sn=2b8c0ed80b684b4284221667460fd19d&scene=23&srcid=1209xMI6SVfocytUqn0WrdHn#rd)

20151210
-------------
* isaced -- [HTTP content-type与AFNetworking](http://www.isaced.com/post-254.html)，是searilization相关，对返回结果进行序列化和格式化。
* CocoaChina -- [那些不能错过的Xcode插件](http://www.cocoachina.com/industry/20130918/7022.html)，觉得VVDocument和XVim插件不错哦。
* CocoaChina -- [专业程序员必习，最牛逼的编码套路](http://www.cocoachina.com/programmer/20151125/14365.html)

20151211
--------------
* segmentfault -- [当我们谈论网络时候，我们在谈论什么（一）：我们如何接入因特网](http://segmentfault.com/a/1190000004094420)，说到了路由器、交换机的作用，说到到分配IP的过程，说到Mac地址的作用，然而我并没有看懂额。
* segmentfault -- [当我们谈论网络时候，我们在谈论什么（二）：DNS的工作原理](http://segmentfault.com/a/1190000004127680)，DNS（Domain Name System），就是域名系统喽，就是把在上网的时候，将浏览器输入的域名--www.baidu.com for example，转换成对应的IP地址。其实我们访问网络，就是访问远程主机的资源了吧。
* CIMGF(Cocoa is My Girl Friend) -- [Cocoa Tutorial NSOperation and NSOperationQueue](http://www.cimgf.com/2008/02/16/cocoa-tutorial-nsoperation-and-nsoperationqueue/)
* stackoverflow -- [NSOperation on iPhone](http://stackoverflow.com/questions/830218/nsoperation-on-the-iphone)，一些不错的回答。
* Apple Document -- [Selector](https://developer.apple.com/library/ios/documentation/General/Conceptual/DevPedia-CocoaCore/Selector.html)，说明了一下selector的作用和简单使用。
* NSHipster -- [NSOperation](http://nshipster.com/nsoperation/)

20151214 - Monday
--------------
* CocoaChina -- [AFNetworking 2.0源代码解析（一）](http://www.cocoachina.com/ios/20140829/9480.html)

##### A.锁
AFURLConnectionOperation 有一把递归锁，再所有会访问/修改成员变量的对外接口都加了锁，因为这些对外的接口用户是可以在任意线程调用的，对于访问和修改成员变量的接口，必须用递归锁保证线程安全。

##### B.序列化
AFNetworking多数类都支持序列化，但实现的是NSSecureCoding的接口，而不是NSCoding，区别在于“解码”数据时候需要指定Class，用-decodeObjectOfClass:forKey:方法代替了-decodeObjectForKey:。这样做更加安全，因为序列化后的数据有可能被篡改，若不指定Class，-decde出来的对象可能不是原来的对象，有潜在风险。另外，NSSecureCoding是iOS 6以上才有的。
这里在序列化时，保存了当前任务状态，接收的数据等，但回调block是保存不了的，需要在取出来发送时候重新设置。可以向下面这样持久化保存和取出任务：
```Objective-C
AFHTTPRequestOperation *operation = [[AFHttpRequestOperation alloc] initWithRequest:request];
NSData *data = [NSKeyedArchiver archivedDataWithRootObject:operation];

AFHTTPRequestOperation *operationFromDB = [NSKeyedUnarchiver unarchiveObjectWithData:data];
[operationFromDB start];
```
* cnblog -- [python爬虫学习系列教程](http://www.cnblogs.com/xin-xin/p/4297852.html)

20151215 - Tuesday
----------------
* CSDN - [iOS TableView中cell的重用reuse机制分析](http://blog.csdn.net/kiki1985/article/details/8772213)

###### 重用实现分析
查看UITableView头文件，会找到NSMutableArray *visiableCells和NSMutableDictionary *reuseableTableCells两个结构，visiableCells内保存当前显示的cells，reuseableTableCells保存可重用的 cells。
TableView显示之初，reuseableTableCells为空，那么[table dequeueReusableCellWithIdentifier:kCellIdentifier];返回nil。开始的cell都是通过[[UITableViewCell alloc] initWithStyle:UITableViewCellStyleDefault reuseIdentifier:kCellIdentifier];来创建，而且cellForRowAtIndexPath只是调用最大显示cell数的次数。
比如：有100条数据，iPhone一屏幕最多显示10个cell，程序最开始显示TableView的情况如下，

首先，用[[UITableViewCell alloc] initWithStyle:UItableViewCellStyleDefault reuseIdentifier:kCellIdentifier]创建十个cell，并且给cell制定同样的重用标识，并且10个cell全部添加到visiableCells数组，reusableTableCells为空；

接着，向下拖动tableView，当cell1完全移动出屏幕，并且cell11完全显示出来的时候，cell11添加到visiableCell数组，cell1移动出visiableCells数组，cell1加入到reuseableTableCells字典中；

接下来，继续向下拖动tableView，因为reusableTableCells中已经有值，所以，当需要显示新的cell，cellForRowAtIndexPath再次被调用的时候，[tableView dequeueReusableCellWithIdentifierLkCellIdentifier]，返回cell1。cell1加入到visiableCells，cell1移除reusableTableCells。
以上，整个过程并不难理解，但需要注意正式这样的原因，配置 cell的时候一定要注意，对去除的重用的cell做重新复制，不要遗留老的数据。

* segmentfault -- [漫谈iOS程序的证书和签名机制](http://segmentfault.com/a/1190000004144556)，这篇文章说的真的不错，对于证书和代码签名的解释值得反复回味，其实我到现在还是有很多的不明白啊，特别是公钥和私钥产生的方式，还是要不断地想啊想啊。
* segmentfault -- [fir.im Weekly - 94 个 iOS 开发资源推荐](http://segmentfault.com/a/1190000004143765)，这里面有不少的swift资源链接，也有相关的github源代码，如果想要学习swift，可以好好看一看拉。

20151217 -- Thursday
---------------------
* CocoaChina -- [AFNetworking源码解析<一>](http://www.cocoachina.com/ios/20140829/9480.html)
* CocoaChina -- [AFNetworking源码解析<二>](http://www.cocoachina.com/ios/20140904/9523.html)
* CocoaChina -- [AFNetworking源码解析<三>](http://www.cocoachina.com/ios/20140916/9632.html)
* CocoaChina -- [AFNetworking源码解析<四>](http://www.cocoachina.com/ios/20141120/10265.html)

20151223 -- Wednesday
--------------
* CodingPy -- [自己动手开发网络服务器（一）](http://codingpy.com/article/build-a-simple-web-server-part-one/)
* Codingpy -- [自己动手开发网络服务器（二）](http://codingpy.com/article/build-a-simple-web-server-part-two/)
* CSDN -- [夜深人静写算法（一）搜索入门](http://www.cppblog.com/menjitianya/archive/2015/10/09/211980.html)

20151228 -- Monday
-------------
* stackoverflow -- [whose view is not in the window hierarchy](http://stackoverflow.com/questions/11862883/whose-view-is-not-in-the-window-hierarchy)

20151229 -- Tuesday
------------------
* skyfox -- [iOS学习路线](http://ios.skyfox.org/route.html)
* 知乎专栏 -- [如何用Github去管理你的Idea](http://zhuanlan.zhihu.com/phodal/20442311)
* 知乎专栏 -- [为什么你应该先成为全栈工程师](http://zhuanlan.zhihu.com/phodal/20439045)
* 直呼专栏 -- [成为一名优秀的Developer的书单](http://zhuanlan.zhihu.com/phodal/20436712)

20160104 -- Monday
-------------
* csdn -- [专栏：Python爬虫入门教程](http://blog.csdn.net/column/details/why-bug.html)

20160106 -- Wensday
-------------
* 知乎 -- [Unicode和UTF-8的区别](http://www.zhihu.com/question/23374078)

20160113 -- Wensday
-----------
* aosabook - [Secrets of Mobile Network Performance](http://aosabook.org/en/posa/secrets-of-mobile-network-performance.html)
* product.hubspot - [Using CocoaPods to Modularize a big iOS app](http://product.hubspot.com/blog/architecting-a-large-ios-app-with-cocoapods)

20160114 -- Thursday
--------
* 360Document - [跳转到App Store的两种方式-直接跳转和应用内跳转](http://www.360doc.com/content/15/0914/18/8772388_499127122.shtml)
* CSDN - [iOS7跳转到App Store评分](http://blog.csdn.net/yangzhen19900701/article/details/42706189)

20160119 -- Tuesday
------------
* Stackoverflow - [What does enable_bitcode do in Xcode7](http://stackoverflow.com/questions/30722606/what-does-enable-bitcode-do-in-xcode-7)
* Quora - [What is Apple bitcode](https://www.quora.com/What-is-Apple-Bitcode)
* Apple Document - [App thinning](https://developer.apple.com/library/tvos/documentation/IDEs/Conceptual/AppDistributionGuide/AppThinning/AppThinning.html)

20160120 -- Wednesday
* Stackoverflow - [Native facebook app does not open with facebook login](http://stackoverflow.com/questions/32566734/native-facebook-app-does-not-open-with-facebook-login-in-ios-9)

20160128 -- Thursday
* cnblog - [三十分钟入门正则表达式](http://www.cnblogs.com/jy578154186/archive/2012/10/22/2734262.html)
