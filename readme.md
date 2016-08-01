
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
注：  位置                 宽高  左填充 背景颜色            /* font-size: 14px;
															   font-family: 微软雅黑; <=>  font:14px/35px 微软雅黑;
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
###20160801
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
9.当有图片插入时，<img src="">
最好给img设定一个宽度或高度，防止其对页面布局错位															
10.元素浮动之后，页面就支持宽高了，所以有宽高即可，display：incline-block 可以去掉																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																