
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

																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																
																