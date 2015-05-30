
#Personal Android Open Source Projects
##Android开源项目收集

----------


###1、[sticky-headers-recyclerview](https://github.com/timehop/sticky-headers-recyclerview)
GroupName滑动到顶端时会固定不动直到另外一个GroupName到达顶端的ListView，采用support-v7中的RecyclerView实现

项目地址：[https://github.com/timehop/sticky-headers-recyclerview](https://github.com/timehop/sticky-headers-recyclerview)

![sticky-headers-recyclerview](http://7xj445.com1.z0.glb.clouddn.com/sticky-headers-recyclerview.gif)

###2、[Material Calendar View](https://github.com/prolificinteractive/material-calendarview)
>A better looking implementation of Android's CalendarView. The goal is to have a more Material look and feel, rather than 100% parity with the platform's implementation.

一个很棒的日历视图控件，没有使用GridView，而是采用ViewPager、LinearLayout、CheckedTextView等组件生成。

项目地址[https://github.com/prolificinteractive/material-calendarview](https://github.com/prolificinteractive/material-calendarview)

![Material Calendar View](http://7xj445.com1.z0.glb.clouddn.com/MaterialCalendarView.gif)
###3、[EfficientAdapter](https://github.com/StanKocken/EfficientAdapter)
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

![](http://git.oschina.net/zhyihui/android-open-projects/raw/master/screenshots/ObservableScrollView_1.gif)![](http://i1.tietuku.com/bb8e294d80f85abe.gif)![](http://i1.tietuku.com/6a0ce1081f864b13.gif)![](http://i1.tietuku.com/1413ac71e6958f89.gif)

更多示例动态图片请到该项目的Github主页上查看。