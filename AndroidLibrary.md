<br/>

该部分主要包括不错的Android开发工具库，这些工具可以或简化我们的开发，或提升App性能，或解决Android版本兼容等。

---

### >>> [okhttp](http://square.github.io/okhttp/)
An HTTP & SPDY client for Android and Java applications. 

OkHttp是Square的一款产品，是一个Java的开源HTTP和SPDY客户端开发包，支持Android。Android自带的两个HTTP框架（HttpURLConnection和HttpClient），在各种Android OS版本一直充斥着错误，可以使任何理智的开发者走向崩溃。不过幸运地是，OkHttp解决了这些问题。OkHttp是建立在HttpUrlConnection上，从Android代码库保持最新的修复，这意味着再也没有与旧操作系统版本出现兼容性问题的噩梦。
>OkHttp is an HTTP client that’s efficient by default:
* 支持SPDY和HTTP/2, 可以合并多个到同一个主机的请求.
* 使用连接池技术减少请求的延迟(如果SPDY是可用的话).
* 使用GZIP压缩减少传输的数据量.
* 缓存响应避免重复的网络请求.

github地址：[https://github.com/square/okhttp](https://github.com/square/okhttp)


### >>> [Retrofit](http://square.github.io/retrofit/)

> A type-safe HTTP client for Android and Java

retrofit 与 okhttp 共同出自 Square 公司，retrofit就是对okhttp做了一层封装。把网络请求都交给给了Okhttp，我们只需要通过简单的配置就能使用retrofit来进行网络请求了。

Github：[http://github.com/square/retrofit](http://github.com/square/retrofit)

### >>> [RxJava](https://github.com/bboyfeiyu/AndroidEventBus)

ReactiveX 是 Reactive Extensions 的缩写，一般简写为 Rx，最初是 LINQ 的一个扩展，由微软的架构师 Erik Meijer 领导的团队开发，在2012年11月开源，Rx是一个编程模型，目标是提供一致的编程接口，帮助开发者更方便的处理异步数据流。

Rx 近几年越来越流行了，现在已经支持几乎全部的流行编程语言了，Rx 的大部分语言库由 ReactiveX 这个组织负责维护。

Netflix 参考微软的 Reactive Extensions 创建了 Java 的实现 RxJava，主要是为了简化服务器端的并发。

RxJava也在Android开发中得到广泛的应用。

> Reactive Extensions for the JVM

> a library for composing asynchronous and event-based programs using observable sequences for the Java VM.（一个在 Java VM 上使用可观测的序列来组成异步的、基于事件的程序的库）

ReactiveX官网：[http://reactivex.io/](http://reactivex.io/)

### >>> [RxAndroid](https://github.com/ReactiveX/RxAndroid)

> Reactive Extensions for Android

RxAndroid来源于RxJava, 在RxJava的基础上扩展了一些Android的功能，主要是为 Android 的主线程提供 Scheduler。

### >>> [AndroidEventBus](https://github.com/bboyfeiyu/AndroidEventBus)
>这是一个Android平台的事件总线框架, 它简化了Activity、Fragment、Service等组件之间的交互，很大程度上降低了它们之间的耦合，使得我们的代码更加简洁，耦合性更低，提升我们的代码质量。

相对于AndroidEventBus，或者大家更熟悉greenrobot的[EventBus](https://github.com/greenrobot/EventBus)，一句话概括EventBus就是：EventBus是一个发布 / 订阅的事件总线。

而AndroidEventBus也是这么一个工具库，而且在易用性上表现更为优秀（作者的意思是性能不如EventBus，但使用更加方便，可以适用更多场景）；AndroidEventBus的作者是中国开发者[bboyfeiyu](https://github.com/bboyfeiyu)，它与EventBus的具体区别处可以参照其Github主页。

项目地址：https://github.com/bboyfeiyu/AndroidEventBus

作者博客：http://www.devtf.cn/



### >>> [Glide](https://github.com/bumptech/glide)
An image loading and caching library for Android focused on smooth scrolling

Glide 是一个 Android 上的图片加载和缓存库，其目的是实现平滑的图片列表滚动效果。

Glide和Picasso非常相似，Glide加载图片的方法和Picasso如出一辙。
>Glide is a fast and efficient open source media management and image loading framework for Android that wraps media decoding, memory and disk caching, and resource pooling into a simple and easy to use interface.

项目地址：[https://github.com/bumptech/glide](https://github.com/bumptech/glide)

jar包下载：[https://github.com/bumptech/glide/releases](https://github.com/bumptech/glide/releases)

### >>> [glide-transformations](https://github.com/wasabeef/glide-transformations)
    
> An Android transformation library providing a variety of image transformations for Glide.

glide-transformations是一个图像转换类库，为Glide（一个快速高效的Android媒体管理框架）提供各种各样的图像转换。


### >>> [logger](https://github.com/orhanobut/logger)

> Simple, pretty and powerful logger for android

Logger provides（Logger提供的特性如下） :

* Thread information
* Class information
* Method information
* Pretty-print for json content
* Pretty-print for new line "\n"
* Clean output
* Jump to source