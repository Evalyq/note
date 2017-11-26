###textarea点击文字消失
	resize:none;  
	<textarea name="" node-type="textarea" class="text" placeholder="有事没事说两句..."onfocus="this.placeholder=''" onblur="this.placeholder='有事没事说两句...'"></textarea>
###文本
	text-shadow：10px下 10px右 10px颁奖 #fff;
	text-indent:缩进
	word-break:break-all;字符断行
	word-wrap:break-word;单词断行
	white-sapce：nowrap;强行显示一行
	overflow:hidden;
	text-overflow:ellipsis;显示省略号
	box-shadow:10px横向 10px竖向 10px #ccc;
	background-size：cover;背景图片铺满
	transform：rotate(30deg) scale(1.5)放大缩小 translate(20px水平，30px) skew倾斜(30deg,30deg)；
	transition:平滑过度什么属性transform(或者all) 1s ease-in/ease-in-out
	animation:donghua 20s infinite一直播放2只播放两次 ease;

		@keyframes donghua{
		   from {top:0px;}
		   to {top:200px;}
		}
		@keyframes testanimations {
			from { transform: translate(0, 0); }
			20% { transform: translate(20px, 20px); }
			40% { transform: translate(40px, 0); }
			60% { transform: translate(60px, 20); }
			80% { transform: translate(80px, 0); }
			to { transform: translate(100px, 20px); }
		}
		@keyframes testanimations{
			0% { transform: translate(0, 0); }
			20% { transform: translate(20px, 20px); }
			40% { transform: translate(40px, 0); }
			60% { transform: translate(60px, 20px); }
			80% { transform: translate(80px, 0); }
			100% { transform: translate(100px, 20px); }
		}
###渐变
线性渐变 
     
		background：gradient(linear,left top,left bottom,from(blue),to(red),color-stop(0.4,#fff),色标color-stop(0.7,green));
径向渐变
  
       background：gradient(radial,center center,0,center center,200,from(blue),to(red))
@media screen and (min-width:900px;)