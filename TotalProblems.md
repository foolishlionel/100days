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

20160201 -- Monday
* csdn - [VPN原理及实现](http://blog.csdn.net/dog250/article/details/5588607)
* h3c - [技术点详解 -- SSL VPN](http://www.h3c.com.cn/MiniSite/Technology_Circle/Technology_Column/ICG/ICG_Technology/201008/686807_97665_0.htm)

20160307 -- Monday
-----------------
Yoho Application是公司主打的一款资讯浏览的App，该App主要包括普通资讯浏览、热门视频播放、电子杂志阅读、内容分享到各大社交平台等基础功能。这款App开发的初衷是将公司的杂志业务从线下迁移到线上，并且在推广过程中找到了新的用户关注点。Yoho iOS版本上架App Store一周时间就冲击到了潮流资讯类App的榜首，这并不是一个偶然，一款App是否吸引人，主要是看这款App的内容是否丰富、使用是否流畅、用户交互是否合理，Yoho作为一款资讯浏览App，主打“内容为王”，及时发布、更新最新的潮流资讯，并且对用户体验不断优化。

#### 2.Yoho App的主要功能
总体来说，这款App主要的功能如下所列，

* 最新最全的潮流资讯阅读
* Yoho男刊、女刊电子杂志的下载和阅读
* 高清优美的壁纸图片下载
* 辅助推广Yoho!Buy电商项目的商品
* 与签约潮流品牌合作，推广多种品牌的服饰和球鞋

#### 3.开发Yoho App所做的任务
作为Yoho App的team leader，在开发App的过程中，主要做了以下的工作，

* 统筹需求，确定需求的难点和细节，合理分配组员工作任务
* 采用MVVM设计模式搭建了App的框架
* 使用缓存技术优化了App离线体验
* 实现了App转场和切换的多种动画效果
* 集成了多个平台的第三方登陆和分享功能
* 实现了Html5的杂志下载和离线阅读功能
* 资讯详情页使用html5和原生代码结合，增强用户体验
* 使用Autolayout和Masonry适配了不同尺寸的屏幕

### 20150328
#### noon
1. 20160325周五 - 汇鑫怡触控市
2. 20160319周六 - 景轩好凶
3. 20160313周日 - 动物成tongue KS
4. 20130222元宵节守护
5. 20160425凌晨一血


### 20160407
1. 廖雪峰的博客站点，[廖雪峰博客](http://www.liaoxuefeng.com/)


20160414
==========
1. django web开发，[自强学堂](http://www.ziqiangxuetang.com/django/django-tutorial.html)
2. 


20160418
============
#### bug fix
- [what I learned from hosting octopress blogs to github pages](http://allenyee.me/blog/2013/08/21/what-i-learned-from-hosting-octopress-on-github/)
- [利用octopress部署博客到github](http://ju.outofmemory.cn/entry/98762)
- [利用octopress搭建一个github博客](http://justcoding.iteye.com/blog/1954645)
- [升级Xcode之后VV-Document不能使用的解决办法](http://www.bubuko.com/infodetail-922634.html)
- [pycharm4注册码](http://my.oschina.net/backtract/blog/360666?fromerr=FCvTSmp9)
- [自定义你的octopress博客](http://foggry.com/blog/2014/04/28/custom-your-octopress-blog/)
- [Mac10.9.5 PHP 5.4安装 memcached](http://www.bubuko.com/infodetail-442622.html)

#### good
- [这样好用的ReactiveCocoa，根本停不下来](http://www.cocoachina.com/ios/20150817/13071.html)
- [iOS证书/私钥/代码签名/描述文件](http://blog.csdn.net/lvxiangan/article/details/17306269)
- [iOS开发证书cer，p12文件，mobileprofile许可文件的作用](http://blog.csdn.net/lanergaming/article/details/38785533)
- [SQLite这么娇小可爱，不多了解点不行啊](http://www.cocoachina.com/ios/20150824/13169.html)
- [Uber的github仓库](https://github.com/uber/)
- [iOS Runtime Practice](https://github.com/huang303513/iOSRunTimeExplore/blob/master/README.md?plg_nld=1&plg_uin=1&plg_auth=1&plg_nld=1&plg_usr=1&plg_vkey=1&plg_dev=1)
- [iOS9-Adaption-Tips](https://github.com/ChenYilong/iOS9AdaptationTips)
- [iOS Provisioning Profile（Certificate）和Code Signing详解](http://blog.csdn.net/phunxm/article/details/42685597)
- [Hexo+github域名和绑定的问题](http://www.jianshu.com/p/1d427e888dda)
- [MMDrawerController](http://code4app.com/ios/MMDrawerController/51b3fd056803fa152e000000)
- [github matt大神的个人中心](https://github.com/mattt)
- [python教程，廖雪峰的官方网站](http://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000)
- [download mysql community server](http://dev.mysql.com/downloads/mysql/5.1.html)
- [download mysql workbench](http://dev.mysql.com/downloads/workbench/)
- [what is this？这是一个大神的个人网站吗](http://chrisrisner.com/)

#### STOF
- [UIActivityViewController crash on iOS8 iPads](http://stackoverflow.com/questions/25644054/uiactivityviewcontroller-crashing-on-ios8-ipads)
- [How do I fix the folling brew doctors errors?](http://stackoverflow.com/questions/18806884/how-do-i-fix-the-following-brew-doctor-errors)

#### WXin
- [微信公众平台](https://mp.weixin.qq.com/cgi-bin/frame?t=mass/statement_frame&nav=10005&lang=zh_CN&token=1684043568)
- [微信开放平台](https://open.weixin.qq.com/)
- [如何排版微信公众平台的文章？](http://www.zhihu.com/question/23640203)
- [支付宝Api](https://doc.open.alipay.com/doc2/detail?treeId=59&articleId=103663&docType=1)

#### CocoaChina
- [长篇高能ReactiveCocoa和MVVM入门](http://www.cocoachina.com/ios/20150526/11930.html)
- [iOS9适配教程系列](http://www.cocoachina.com/ios/20150703/12392.html)

#### Github Repo
- [Coding源代码](https://github.com/Coding/Coding-iOS)

#### Photo Collections
- [Awesome Wallpapers](http://alpha.wallhaven.cc/)
- [花瓣网](http://huaban.com/)
- [Mobile Design Pattern](http://pttrns.com/)

#### iOS Push推送原理
- [iOS推送消息，PHP做推送服务器](http://www.cnblogs.com/wenxp2006/articles/2555716.html)
- [细说iOS消息推送](http://www.cocoachina.com/industry/20140528/8582.html)

#### Blogs
- [稀土掘金文章聚合首页](https://xitu.io/)
- [优酷大神ibireme的github博客](http://blog.ibireme.com/)
- [Rannie's Page的个人博客](http://rannie.github.io/)
- [iOS/Mac一些知名开发者的博客站点收藏](http://www.cocoachina.com/bbs/read.php?tid=299721)
- [分分钟学会正则表达式-小芳芳](http://my.oschina.net/joanfen/blog/415076?fromerr=e0NdVQgs)
- [樱空释大神推荐的一个有意思的网站](https://www.tumblr.com/login?redirect_to=%2Fdashboard)
- [isaced的个人博客收藏](http://www.isaced.com/)
- [App素材收藏的网站](https://icomoon.io/app/#/select)
- [iOS CocoaPods使用详细说明](http://blog.csdn.net/showhilllee/article/details/38398119)
- [iOS9适配系列教程-中文版](http://blog.csdn.net/majiakun1/article/details/49072761)
- [iOS开发中NSRunloop和NSTimer的问题](http://www.jianshu.com/p/79c17938953f)
- [iOS事件处理机制和图像渲染过程](http://www.cocoachina.com/ios/20151203/14549.html)
- [小笨狼的gitcafe的博客](http://jiangliancheng.gitcafe.io/)
- [为什么 iPhone 6 Plus 要将 3x 渲染的 2208x1242 分辨率缩小到 1080p 屏幕上？](http://www.zhihu.com/question/25288571)
- [酷壳网站-讨厌百度的IT攻城狮陈皓么？](http://coolshell.cn/)
- [iOS开发之如何跳转到系统设置里面的各个设置界面](http://mp.weixin.qq.com/s?__biz=MjM5OTM0MzIwMQ==&mid=401517056&idx=5&sn=ad89f960098b485035006eef656efe16&scene=23&srcid=12108jodHzn4F5ocD4sh1Qa1#rd)
- [python入门，慕课网的简单教程](http://www.imooc.com/view/177)
- [python2.7教程，廖雪峰的官方网站](http://www.liaoxuefeng.com/wiki/001374738125095c955c1e6d8bb493182103fac9270762a000)
- [python入门之综述](http://cuiqingcai.com/927.html)
- [深圳买房，首付凑不够可以贷款凑首付吗](http://www.zhihu.com/question/31066464)
- [二套房最低首付降至 40% 和营业税起征年限降至 2 年释放出了怎样的信号？](http://www.zhihu.com/question/29167089?rf=29169103)
- [国家开发银行的各个级别的联系人联系方式](http://www.csls.cdb.com.cn/csls.portal.Contact.ActionContactLinkman.do?doType=summary)
- [国家开放银行的贷款信息网站](http://www.csls.cdb.com.cn/page.do?targetPage=/portal/Index.jsp)
- [南京正式启用居住证 哪些人需要办理？](http://njbbs.fang.com/wyjlb~-1/544337968_544337968.htm)
- [多线程之NSOperation简介](http://www.jianshu.com/p/a044cd145a3d)
- [Developer进阶书单](http://phodal.github.io/booktree/)
- [自己手动开发网络服务器](http://codingpy.com/article/build-a-simple-web-server-part-one/)
- [日常使用git的19个建议](http://blog.jobbole.com/96088/)
- [swiftcafe-一个siwft教程的网站](http://swiftcafe.io/)
- [react-native getting started教程](http://facebook.github.io/react-native/docs/getting-started.html)
- [The GeoJSON Format Specification](http://geojson.org/geojson-spec.html)
- [cocos的HelloWorld教程](http://www.cocos.com/docs/creator/getting-started/hello-world.html)
- [csdn-Swift的可选值optional简要介绍](http://blog.csdn.net/weasleyqi/article/details/41347737)
- [vpn原理以及实现--一般理论](http://blog.csdn.net/dog250/article/details/5588607)
- [技术点详解ssl vpn](http://www.h3c.com.cn/MiniSite/Technology_Circle/Technology_Column/ICG/ICG_Technology/201008/686807_97665_0.htm)
- [vpn的实现原理](http://zheng.blog.51cto.com/blog/36119/10754)
- [swift中文版两大官方文档汇总](http://www.cocoachina.com/industry/20140613/8818.html)
- [CocoaChina的Swift专题页](http://www.cocoachina.com/special/swift/)
- [Swift可选值optional values介绍](http://blog.csdn.net/zhangao0086/article/details/38640209)
- [标哥的iOS相关技术的博客](http://www.henishuo.com/)
- [DRRRRRIB的开发者网站](http://developer.dribbble.com/v1/)
- [计组|操作系统|数据结构|网络|码农基本功](http://www.zhihu.com/collection/37506044)
- [知乎的计算机科学收藏夹](http://www.zhihu.com/collection/31108918)
- [github上面的一个swift资源汇总的repo](https://github.com/ipader/SwiftGuide)
- [https科普扫盲贴](https://segmentfault.com/a/1190000004523659)
- [菜鸟教程，学的不仅仅是技术。一些前端技术教程汇总](http://www.runoob.com/)
- [一些基本而又常用的JavaScript语句](http://www.itxueyuan.org/view/6300.html)
- [环信SDK的官方网站](http://www.easemob.com/)
- [多亏Sketch，我这个小码农可以自己设计App了](http://www.jianshu.com/p/c2946a9869ed)
- [深入github主页，是介绍github pages的文章](https://www.awesomes.cn/source/10)
- [深入浅出－iOS的TCP/IP协议族剖析&&Socket](http://www.jianshu.com/p/cc756016243b)
- [swift开发者周刊](http://swiftweekly.cn/archive/weekly20.html)
- [mac系统如何编辑Host文件](http://jingyan.baidu.com/article/8cdccae965875c315413cdfe.html)
- [数据库设计step by step 2，数据库的生命周期](http://www.cnblogs.com/DBFocus/archive/2011/04/09/2010904.html)
- [搭建Hexo博客，并部署到github详细教程](http://blog.sina.com.cn/s/blog_4c44643f0102vuju.html)
- [concise，一款专为hexo设计的漂亮博客主题](http://blog.csdn.net/v123411739/article/details/45227249)
- [hexo:ERROR Deployer not found: github](http://stackoverflow.com/questions/34452547/hexoerror-deployer-not-found-github)
- [利用hexo+github搭建属于自己的博客](http://www.jianshu.com/p/465830080ea9)
- [hexo搭建github静态博客](http://www.cnblogs.com/zhcncn/p/4097881.html)
- [how to percent encode a URL String](http://useyourloaf.com/blog/how-to-percent-encode-a-url-string/)
- [Objective-C url encoding](http://stackoverflow.com/questions/8086584/objective-c-url-encoding)
- [毕设记录，python利用socket进行文件传输](http://www.jianshu.com/p/2a4b859e05df)
- [你听过哪些赚钱的歪点子](http://www.zhihu.com/question/40155967/answer/89133807)
- [swift 2.2的新特性](http://swiftcafe.io/2016/04/07/swift2-2/)
- [iOS项目的目录结构能够看出你的开发经验](http://www.wtoutiao.com/p/E28hSW.html)
- [djangoproject，是django的官方教程](https://www.djangoproject.com/start/overview/)
- [mac下搭建PHP开发环境](http://blog.chinaunix.net/uid-22556372-id-3245808.html)
- [django基础教程-自强学堂](http://www.ziqiangxuetang.com/django/django-tutorial.html)
- [CPU阿甘，通过生动详实的例子来说明CPU运行的流程](http://mp.weixin.qq.com/s?__biz=MzAxOTc0NzExNg==&mid=2665513017&idx=1&sn=5550ee714abd36d0b580713f673e670b#rd)
- [企业微信--让每个企业都有自己的微信](https://itunes.apple.com/app/id1087897068)
- [Yoho企业邮箱账号更改的网站](https://smail.yoho.cn/)


20160420
==============
- [iOS开发中常见问题集锦](http://www.cnblogs.com/Leo_wl/archive/2013/03/06/2946588.html)
- [iOS开发常见疑难问题解决方案大集锦](http://mobile.51cto.com/iphone-407836.htm)
