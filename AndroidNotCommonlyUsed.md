收集一些不常用的 Android 开源项目

### >>> [fresco](https://github.com/facebook/fresco)

>Fresco is a powerful system for displaying images in Android applications.

Fresco 是一个强大的图片加载组件。

Fresco 中设计有一个叫做 image pipeline 的模块。它负责从网络，从本地文件系统，本地资源加载图片。为了最大限度节省空间和CPU时间，它含有3级缓存设计（2级内存，1级文件）。

Fresco 中设计有一个叫做 Drawees 模块，方便地显示loading图，当图片不再显示在屏幕上时，及时地释放内存和空间占用。

Fresco 支持 Android2.3(API level 9) 及其以上系统。

项目地址：https://github.com/facebook/fresco

中文文档：http://fresco-cn.org/docs/index.html

### >>> [EfficientAdapter](https://github.com/StanKocken/EfficientAdapter)
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

### >>> [Netroid](http://netroid.cn/)
>Netroid是一个基于Volley实现的Android Http库。提供执行网络请求、缓存返回结果、批量图片加载、大文件断点下载的常见Http交互功能。致力于避免每个项目重复开发基础Http功能，实现显著地缩短开发周期的愿景。

Netroid在Volley的基础之后作了简化和扩展，使用还是挺简便的。

详情请参见项目主页或者Github主页的介绍和示例。

项目主页：http://netroid.cn/

Github地址：https://github.com/vince-styling/Netroid

## 开源组件
---

### >>> [JazzyListView](https://github.com/twotoasters/JazzyListView)
>JazzyListView is an extension of ListView designed to animate list item views as they become visible. There are a number of pre-built, bundled effects that can be used by setting the effect in code or an XML layout attribute. Also, it is possible to use a custom effect by implementing a JazzyEffect.

>This project was inspired by [stroll.js](http://lab.hakim.se/scroll-effects).

ListView及GridView item以特殊动画效果进入屏幕，效果包括grow、cards、curl、wave、flip、fly等等。

支持RecyclerView。

项目Demo效果可以直接到这里查看：[stroll.js](http://lab.hakim.se/scroll-effects)

项目地址：[https://github.com/twotoasters/JazzyListView](https://github.com/twotoasters/JazzyListView)

### >>> [Android-ObservableScrollView](https://github.com/ksoichiro/Android-ObservableScrollView)

>Android library to observe scroll events on scrollable views.
It's easy to interact with the Toolbar introduced in Android 5.0 Lollipop and may be helpful to implement look and feel of Material Design apps.

监听滚动视图滚动事件的库，帮助与Toolbar的交互动效处理与Material Design的实现;支持ListView、GridView、RecyclerView等组件。

项目地址：[https://github.com/ksoichiro/Android-ObservableScrollView](https://github.com/ksoichiro/Android-ObservableScrollView)

![](http://git.oschina.net/zhyihui/awesome-projects/raw/master/screenshots/ObservableScrollView_1.gif)![](http://git.oschina.net/zhyihui/awesome-projects/raw/master/screenshots/ObservableScrollView_2.gif)![](http://git.oschina.net/zhyihui/awesome-projects/raw/master/screenshots/ObservableScrollView_3.gif)![](http://git.oschina.net/zhyihui/awesome-projects/raw/master/screenshots/ObservableScrollView_4.gif)

更多示例动态图片请到该项目的Github主页上查看。

### >>> [PagerSlidingTabStrip](https://github.com/astuetz/PagerSlidingTabStrip)

**Android Support 中已包含 TabLayout 控件，以后可能就不用第三方控件了**

>An interactive indicator to navigate between the different pages of a ViewPager

配合ViewPager使用的Indicator(指示器)，支持ViewPager与Indicator联动；可以定制指示器颜色、Tab字体等属性。

项目地址：[https://github.com/astuetz/PagerSlidingTabStrip](https://github.com/astuetz/PagerSlidingTabStrip)

![](http://7xj445.com1.z0.glb.clouddn.com/PagerSlidingTabStrip.png) ![](http://7xj445.com1.z0.glb.clouddn.com/PagerSlidingTabStrip_2.png)