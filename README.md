
#Personal Android Open Source Projects Collection   
##-------------- Android开源项目收集

----------  

<br/>

##一、组件篇
----
这一部分主要收集了一些优秀的自定义控件，这些控件弥补了Android SDK的不足，使App更加友好和美观。

###1、[sticky-headers-recyclerview](https://github.com/timehop/sticky-headers-recyclerview)
GroupName滑动到顶端时会固定不动直到另外一个GroupName到达顶端的ListView，采用support-v7中的RecyclerView实现

项目地址：[https://github.com/timehop/sticky-headers-recyclerview](https://github.com/timehop/sticky-headers-recyclerview)

![sticky-headers-recyclerview](http://7xj445.com1.z0.glb.clouddn.com/sticky-headers-recyclerview.gif)

###2、[Material Calendar View](https://github.com/prolificinteractive/material-calendarview)
>A better looking implementation of Android's CalendarView. The goal is to have a more Material look and feel, rather than 100% parity with the platform's implementation.

一个很棒的日历视图控件，没有使用GridView，而是采用ViewPager、LinearLayout、CheckedTextView等组件生成。

项目地址[https://github.com/prolificinteractive/material-calendarview](https://github.com/prolificinteractive/material-calendarview)

![Material Calendar View](http://7xj445.com1.z0.glb.clouddn.com/MaterialCalendarView.gif)

###4、[android-Ultra-Pull-To-Refresh](https://github.com/liaohuqiu/android-Ultra-Pull-To-Refresh)

这是现在已经停止维护的下拉刷新项目的替代方案；继承于ViewGroup可以包含任何View；功能比SwipeRefreshLayout强大。

此项目的Demo截图很多，可以到其Github主页上查看，功能十分丰富，使用却很简单。

![android-Ultra-Pull-To-Refresh](http://7xj445.com1.z0.glb.clouddn.com/android-Ultra-Pull-To-Refresh.gif)

项目地址：[https://github.com/liaohuqiu/android-Ultra-Pull-To-Refresh](https://github.com/liaohuqiu/android-Ultra-Pull-To-Refresh)

###5、[JazzyListView](https://github.com/twotoasters/JazzyListView)
>JazzyListView is an extension of ListView designed to animate list item views as they become visible. There are a number of pre-built, bundled effects that can be used by setting the effect in code or an XML layout attribute. Also, it is possible to use a custom effect by implementing a JazzyEffect.

>This project was inspired by [stroll.js](http://lab.hakim.se/scroll-effects).

ListView及GridView item以特殊动画效果进入屏幕，效果包括grow、cards、curl、wave、flip、fly等等。

支持RecyclerView。

项目Demo效果可以直接到这里查看：[stroll.js](http://lab.hakim.se/scroll-effects)

项目地址：[https://github.com/twotoasters/JazzyListView](https://github.com/twotoasters/JazzyListView)

###6、[PagerSlidingTabStrip](https://github.com/astuetz/PagerSlidingTabStrip)

>An interactive indicator to navigate between the different pages of a ViewPager

配合ViewPager使用的Indicator(指示器)，支持ViewPager与Indicator联动；可以定制指示器颜色、Tab字体等属性。

项目地址：[https://github.com/astuetz/PagerSlidingTabStrip](https://github.com/astuetz/PagerSlidingTabStrip)

![](http://7xj445.com1.z0.glb.clouddn.com/PagerSlidingTabStrip.png) ![](http://7xj445.com1.z0.glb.clouddn.com/PagerSlidingTabStrip_2.png)

###7、[Android-ObservableScrollView](https://github.com/ksoichiro/Android-ObservableScrollView)

>Android library to observe scroll events on scrollable views.
It's easy to interact with the Toolbar introduced in Android 5.0 Lollipop and may be helpful to implement look and feel of Material Design apps.

监听滚动视图滚动事件的库，帮助与Toolbar的交互动效处理与Material Design的实现;支持ListView、GridView、RecyclerView等组件。

项目地址：[https://github.com/ksoichiro/Android-ObservableScrollView](https://github.com/ksoichiro/Android-ObservableScrollView)

![](http://git.oschina.net/zhyihui/android-open-projects/raw/master/screenshots/ObservableScrollView_1.gif)![](http://git.oschina.net/zhyihui/android-open-projects/raw/master/screenshots/ObservableScrollView_2.gif)![](http://git.oschina.net/zhyihui/android-open-projects/raw/master/screenshots/ObservableScrollView_3.gif)![](http://git.oschina.net/zhyihui/android-open-projects/raw/master/screenshots/ObservableScrollView_4.gif)

更多示例动态图片请到该项目的Github主页上查看。

##二、工具库
----
该部分主要包括不错的Android开发工具库，这些工具可以或简化我们的开发，或提升App性能，或解决Android版本兼容等。
###1、[EfficientAdapter](https://github.com/StanKocken/EfficientAdapter)
>An efficient adapter to make the use of RecyclerView much easier.

使用这个适配器之后，我们可以只定义ViewHolder，不需要再写Adapter了；我们需要像下面这样定义一个ViewHolder（继承自EfficientAdapter的AbsViewHolder类：

    public class BookViewHolder extends AbsViewHolder<Book> {
    	public BookViewHolder(View itemView) {  
			super(itemView); 
		}

    	@Override
    	protected void updateView(Context context, Book object) {
    	    TextView textView = (TextView) findViewByIdEfficient(R.id.title_textview);
    	    textView.setText(object.getTitle());
    	}
	}
然后就可以设置到RecyclerView中：

	SimpleAdapter adapter = new SimpleAdapter<Plane>(R.layout.item_book, BookViewHolder.class, listOfBooks);
	recyclerView.setAdapter(adapter);
做完以上两步就可以了。

项目地址：[https://github.com/StanKocken/EfficientAdapter](https://github.com/StanKocken/EfficientAdapter)

###2、[AndroidEventBus](https://github.com/bboyfeiyu/AndroidEventBus)
>这是一个Android平台的事件总线框架, 它简化了Activity、Fragment、Service等组件之间的交互，很大程度上降低了它们之间的耦合，使得我们的代码更加简洁，耦合性更低，提升我们的代码质量。

相对于AndroidEventBus，或者大家更熟悉greenrobot的[EventBus](https://github.com/greenrobot/EventBus)，一句话概括EventBus就是：EventBus是一个发布 / 订阅的事件总线。

而AndroidEventBus也是这么一个工具库，而且在易用性上表现更为优秀（作者的意思是性能不如EventBugs，但使用更加方便，可以适用更多场景）；AndroidEventBus的作者是中国开发者[bboyfeiyu](https://github.com/bboyfeiyu)，它与EventBus的具体区别处可以参照其Github主页。

项目地址：https://github.com/bboyfeiyu/AndroidEventBus

作者博客：http://www.devtf.cn/

##3、[Netroid](http://netroid.cn/)
>Netroid是一个基于Volley实现的Android Http库。提供执行网络请求、缓存返回结果、批量图片加载、大文件断点下载的常见Http交互功能。致力于避免每个项目重复开发基础Http功能，实现显著地缩短开发周期的愿景。

Netroid在Volley的基础之后作了简化和扩展，使用还是挺简便的。

详情请参见项目主页或者Github主页的介绍和示例。

项目主页：http://netroid.cn/

Github地址：https://github.com/vince-styling/Netroid