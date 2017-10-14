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
+ 定位 
+ 宽度高度 
+ 颜色字体

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
###tab切换
    $(function(){
	   	   $(".tab ul li").click(function(){
               $(this).addClass("select").siblings().removeClass("select");
               var index =$(this).index();
               $(".conbox div").eq(index).show().siblings().hide();
	   	   })
    })