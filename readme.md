
##电商购物网站

###20160728 
只做了一个导航栏布局

###20160729
CommonStyle
1.重置样式 清零 清浮动
2.input select textarea  
轮廓 outline:0;
边框 borer:0



第一部分  顶部+导航条
1.顶部结构
top 左右分布 左右浮动
左                  右
图标+文字         文字
注：文字颜色 加粗 左右填充li
2.顶部细化
       左                      左                              右
     logo图片                 搜索框                        购物车 图标+字体
注：  位置                 宽高  左填充 背景颜色          /* font-size: 14px;
														 font-family: 微软雅黑; <=>font:14px/35px 微软雅黑;
															line-height: 35px;*/
															text-indent:40px;//首行缩进40px

###20160729																
3.导航
(1)全部商品下拉
	下拉图标安放< i >< /i >																
(2)右面ul  li 依次横排 float:left
(3)下拉列表 字体 四周填充   右侧图标															
(4)下拉列表absolute 与全部商品下拉relative 定位
4.右侧商品分类展示
dl dt dd
padding: 
padding:10px 5px 15px 20px;

    上内边距是 10px
    右内边距是 5px
    下内边距是 15px
    左内边距是 20px
padding:10px 5px 15px;

    上内边距是 10px
    右内边距和左内边距是 5px
    下内边距是 15px
padding:10px;

    所有 4 个内边距都是 10px
###20160801 滚动图片 banner+主列表左侧
5.定义下面两个样式 控制模块显示或隐藏
.hide{
    display: none;
}
.show{
    display: block;
}
6.Banner横幅广告																
overflow 属性规定当内容溢出元素框时发生的事情。																
		visible 	默认值。内容不会被修剪，会呈现在元素框之外。
		hidden 	内容会被修剪，并且其余内容是不可见的。
		scroll 	内容会被修剪，但是浏览器会显示滚动条以便查看其余的内容。
		auto 	如果内容被修剪，则浏览器会显示滚动条以便查看其余的内容。															
7.内线元素 显示
display:inline-block
8.图片上显示滑动图标
     父类                       banner_bar position:relative
      图片                     imgBox	   position:absolute
图片上的滑动图标imgNum           position:absolute																
9.当有图片插入时，< img src="">
最好给img设定一个宽度或高度，防止其对页面布局错位															
10.元素浮动之后，页面就支持宽高了，所以有宽高即可，display：incline-block 可以去掉																
20160802  主列表右侧  

20160803  
首页底部   
1.背景灰色 width:100% 
2.commonWidth:1000px;
3.行高 height:24px   text-align:center 剧中
3.< p>中文字< a> color：#000 及a:hover {color:red}
5.图片 padding-top:30px  图片间距 margin:0 10px;

产品分类左导航栏
1.左导航栏和右侧banner部分 是左右两个模块  左侧导航栏  width:180px 向左浮动
											banner   width:810px  向右浮动
2.左侧导航栏 背景颜色 边宽 
  其中包含产品标题和产品列表两部分
  产品标题  字体大小 粗细  行高(垂直方向剧中) text-align:center(水平方向剧中)
  产品列表  距离上下左右边框距离padding:0 18px 4px;   
  			标题h3  行高 字体
  			列表ul li  两列 li宽度width:50%; 向左浮动

产品分类列表
1.包括标题和商品展示两部分 与banner距离用div 其height:7px
2.由于标题下方有一个灰色的长下划线和蓝色的短下划线，因此标题放在一个div中  
	div 行高 下划线2px的灰色实线
	标题 下划线1px的蓝色实线
3.下方商品列表展示
每一个模块都是图片+文字+价格+评价 每个的宽度为25%  间距margin:0 10px;
模块用两层div嵌套  这样能防止每一行的第四个图片掉下来
 外层 padding: 0 10px;
 内层 width：25%；margin:0 10px; 向左浮动
文字  大小 字体 行高 a:hover 
价格  字体颜色 加粗 上边距margin-top:10px或者padding-top:10px 都能达到效果
评价 星级  用< span> 设置span 高度 宽度 overflow:hidden 间距  内嵌元素展示需有 display：inline-block  

###20160805
产品筛选模块
产品列表左侧区域
1.产品列表只有一列 li width:auto
2.标题字体大小 font-family
产品筛选
1.产品筛选标题 筛选商品名称
dl dt dd  
dt 高度 宽度 行高 左浮动
dd 宽度 右边距 浮动
2.商品展示
三列 33.3% 图片 文字+价格+加入购物车
问题：商品展示浏览器兼容问题？？？
IE和firefox 展示正常，而google浏览器商品展示错位，明天将解决这个问题。


###20160806
问题解答：商品展示浏览器兼容问题？？
刚开始调的时候，我一直以为是左右padding的问题，把左右padding减小，在google和IE上仍会出现商品展示错位问题，然后我把问题归结到向下错位的模块上，把这个div复制几份，显示都正常；后来突然看到错位模块的上一个div的height和其它的相比较小，突然领悟问题应该是处在没有给这个div控制高度。我打开了京东的网站，用firebug调节显示一下，看到都给每个item定有一个高度，所以我把height设定好之后，再在几个浏览器上测试，显示均正常。


display属性
		block 	此元素将显示为块级元素，此元素前后会带有换行符。
		inline 	默认。此元素会被显示为内联元素，元素前后没有换行符。
		inline-block 	行内块元素	

分页
上一页 数字 下一页 放在< a>标签里;文字 span;按钮
设置 高度 宽度 行高 剧中 padding 	边框等等
###20160807													
产品介绍																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																