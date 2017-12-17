###权重 
元素选择器1，类选择器10，id选择器100 行内样式1000；

**文档流**:从上到下从左到右 浮动,position：脱离文档流 无位置（根据内容决定）
#####（是否独占一行）#####
行内元素(display:inline)：a span img textarea 

块内元素(display:block)：h标签 li  ul table hr pre
 
清除浮动 clearfix：浮动元素的父级

**盒子模型**：content padding border margin

一个有宽度的元素才能用margin:0 auto;

###定位属性
+ Relative 原来的位置
+ Absolute 距离最近具有定位属性的父元素   根元素
+ Fixed 相对浏览器窗口

###代码书写顺序
+ 位置属性
+ 宽度高度 
+ 颜色字体
+ 背景（border)
+ animation,tansition


###代码起名规范
+ 导航：nav
+ 侧栏：sidebar
+ 栏目：column
+ 登录条：loginbar
+ 广告：banner
+ 子导航：subnav
+ 子菜单：submenu
+ 版权：copyright
+ 标签：tags
+ 提示信息：msg
+ 小技巧：tips
+ 指南：guild
注释的写法:
/* Header */
内容区
/* End Header */
id的命名:
1)页面结构
容器: container
页头：header
内容：content/container
页面主体：main
页尾：footer
导航：nav
侧栏：sidebar
栏目：column
页面外围控制整体佈局宽度：wrapper
左右中：left right center
(2)导航
导航：nav
主导航：mainbav
子导航：subnav
顶导航：topnav
边导航：sidebar
左导航：leftsidebar
右导航：rightsidebar
菜单：menu
子菜单：submenu
标题: title
摘要: summary
(3)功能
标志：logo
广告：banner
登陆：login
登录条：loginbar
注册：regsiter
搜索：search
功能区：shop
标题：title
加入：joinus
状态：status
按钮：btn
滚动：scroll
标籤页：tab
文章列表：list
提示信息：msg
当前的: current
小技巧：tips
图标: icon
注释：note
指南：guild
服务：service
热点：hot
新闻：news
下载：download
投票：vote
合作伙伴：partner
友情链接：link
版权：copyright
注意事项::
1.一律小写;
2.尽量用英文;
3.不加中槓和下划线;
4.尽量不缩写，除非一看就明白的单词。
 
CSS样式表文件命名
主要的 master.css
模块 module.css
基本共用 base.css
布局、版面 layout.css
主题 themes.css
专栏 columns.css
文字 font.css
表单 forms.css
补丁 mend.css
打印 print.css

**xmp和prev**

xmp的标签，会把抱在内部的html片段当作字符串输出
pre标签，可以在保留原来文本格式的基础上让文本在页面上显示出来

Hover 附加新的样式 
.Clearfix::after
<&lt;     >&gt;
设置整体样式 html,body{}
一个块元素有宽度有高度才能用margin:0 auto;

**box-sizing**

        box-sizing:border-box;
		-moz-box-sizing:border-box; /* Firefox */
		-webkit-box-sizing:border-box; /* Safari */
		box-sizing: content-box|border-box|inherit;


seo查询   h1 logo 
cursor：pointer 光标变手

**弹窗**
    
       {
	    width：100%；
		height：100%；
		position：fixed;
		Top:0;
		Left:0;
	   }
####overflow
+ 单行文本的溢出显示省略号

		{
		overflow: hidden;  
		text-overflow:ellipsis;    
		white-space: nowrap
		}
+ 实现多行文本显示省略号
        {
		display: -webkit-box;
		-webkit-box-orient: vertical;
		-webkit-line-clamp: 3;  显示三行
		overflow: hidden;
		}
###图片水平居中的两种方式

**有宽度跟高度上下左右居中**

    img{
	    position: absolute;
	    width: 200px; 
	    height: 464px;
	    left: 50%;
	    top: 50%;
	    margin-left: -100px;
	    margin-top: -232px;
	   }
	img {
	    position: absolute;
	    width: 200px;
	    height: 464px;
	    left: 0;
	    top: 0;
	    right: 0;
	    bottom: 0;
	    margin: auto;
	}
###重置行高样式
line-height：1；子元素继承父元素的样式 恢复到原来。

**box-shadow**: h-shadow v-shadow blur spread color inset;
             水平        垂直      模糊距离    颜色   内部阴影

###阻止链接跳转的方式
+ javascript:void(0)
+ #

#移动端
###左边固定右边自适应
###图片自适应
     .discuss-item,.doctor-item{
	   	padding:1.5rem 1.5rem 1.5rem 7rem;
	   	position: relative;
	   	background: #FFFFFF;
        border-bottom: 0.5rem solid #f1f1f1;
	   }
	   .discuss-item{
	   	border:0.05rem solid #E7E7E7;
	   }
	   .author-img{
	   	width:4rem;
	   	height:4rem;
	   	border-radius: 100%;
	   	position: absolute;
	   	left:1.5rem;
	   	top:1.5rem;
	   }

**清除input focus样式**

       input:focus{
            outline: none;
         border:1px solid #00b38a; 
        }