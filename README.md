#Personal Android Open Source Projects
-----
###1、[sticky-headers-recyclerview](https://github.com/timehop/sticky-headers-recyclerview)
GroupName滑动到顶端时会固定不动直到另外一个GroupName到达顶端的ListView，采用support-v7中的RecyclerView实现

项目地址：[https://github.com/timehop/sticky-headers-recyclerview](https://github.com/timehop/sticky-headers-recyclerview)

![sticky-headers-recyclerview](http://7xj445.com1.z0.glb.clouddn.com/sticky-headers-recyclerview.gif)

###2、[Material Calendar View](https://github.com/prolificinteractive/material-calendarview)
A better looking implementation of Android's CalendarView. The goal is to have a more Material look and feel, rather than 100% parity with the platform's implementation.

一个很棒的日历视图控件，没有使用GridView，而是采用ViewPager、LinearLayout、CheckedTextView等组件生成。

项目地址[https://github.com/prolificinteractive/material-calendarview](https://github.com/prolificinteractive/material-calendarview)

![Material Calendar View](http://7xj445.com1.z0.glb.clouddn.com/MaterialCalendarView.gif)
###3、[EfficientAdapter](https://github.com/StanKocken/EfficientAdapter)
An efficient adapter to make the use of RecyclerView much easier.

使用这个适配器之后，我们可以只定义ViewHolder，不需要再写Adapter了；我们需要像下面这样定义一个ViewHolder（继承自EfficientAdapter的AbsViewHolder类：

    public class BookViewHolder extends AbsViewHolder<Book> {
    	public BookViewHolder(View itemView) {  super(itemView); }

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