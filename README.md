ListviewHeaderStick
===================
最简单的ListViewHeaderStick，

listview 头部悬浮示例   

原理直接加一个View dyncView， 当成是Listview的headerView
然后dyncView 在滑动的时候设置隐藏和出现

#效果图：
![](https://github.com/lovemelovemydog/ListviewHeaderStick/blob/master/sticky/2014120801.gif)
	
	
##代码使用：
lv.setOnScrollListener(new OnScrollListener() {

			@Override
			public void onScrollStateChanged(AbsListView view, int scrollState) {

			}

			@Override
			public void onScroll(AbsListView view, int firstVisibleItem,int visibleItemCount, int totalItemCount) {
				if (firstVisibleItem >= 1) {
					dyncView.setVisibility(View.VISIBLE);
				} else {
					dyncView.setVisibility(View.GONE);
				}
			}
		});
		
		
	
