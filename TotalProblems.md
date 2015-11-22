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

#### Chrome浏览器的Dolphin爬墙插件
* [Dolphin官方下载地址](https://taobao.com/)
