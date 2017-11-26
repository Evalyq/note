location.href
**获取值**
+ val()  input,textarea;
+ text();
+ html();
var enterUserName =$("input[name='username']").val();
* attr
* removeattr
* prop({ch、ecked:true})
* each()

            $("input[type='checkbox']").each(function(index,item){
                    $(item).prop({checked:!$(item).prop("checked")});
                })//对于每个匹配的元素所要执行的函数

**滚动条fixed根据滚动高度判断位置**

       $(function(){
         $(window).scroll(function(){
        var bottomEndHeight = $(".bottom-end").height();//获取页面的文档高度
        var bodyHeight = $("body").height();//浏览器当前窗口文档body的高度：
        var windowHeight = $(window).height();//获取浏览器显示区域（可视区域）的高度
        var scrollHeight = $(window).scrollTop();//获取滚动条到顶部的垂直高度 (即网页被卷上去的高度) 
        if((scrollHeight + windowHeight) >= (bodyHeight - bottomEndHeight)) {
          $(".bottom-middle").removeClass("bottom-tip")
        }else {
          $(".bottom-middle").addClass("bottom-tip")
        }
      })
      })
**展开收起**

	    $(document).ready(function(){
	      $(".btn1").each(function(){
	        $(this).click(function(){
	            $(this).css("visibility","hidden");
	            $(this).siblings(".box").css("overflow","visible");
	            $(this).siblings(".btn2").css("visibility","visible");
	        })
	    })
	    $(".btn2").each(function(){
	        $(this).click(function(){
	            $(this).css("visibility","hidden");
	            $(this).siblings(".box").css("overflow","hidden");
	            $(this).siblings(".btn1").css("visibility","visible");
	        })
	    })
	   
	});
###tab切换
    $(function(){
	   	   $(".tab ul li").click(function(){
               $(this).addClass("select").siblings().removeClass("select");
               var index =$(this).index();
               $(".conbox div").eq(index).show().siblings().hide();
	   	   })
    })
###轮播
  $(function(){
	  	$(".left").click(function(){
	  		$(".divbox ul").stop(true,true).animate({//结束动画，完成动画·
	  			marginLeft: "-=300px",
	  		},500,function(){
	  			var first=$(".divbox ul li").first();
	  			var last=$(".divbox ul li").last();
	  			first.insertAfter(last);
	  			$(".divbox ul").css("margin-left","-300px")//重置
	  			// $(".divbox ul li"):first().insertAfter($(".divbox ul li"):last());
	  		})
	  	})
	  	$(".right").click(function(){
	  		$(".divbox ul").stop(true,true).animate({
	  			marginLeft:"+=300px",
	  		},500,function(){
	  			var first=$(".divbox ul li").first();
	  			var last=$(".divbox ul li").last();
	  			last.insertBefore(first);
	  			$(".divbox ul").css("margin-left","-300px")
	  		})
	  	})
	  })

###focus方法
          $(".search-in").focus(function(){
                $(".search-hot-words").hide();
            }).blur(function(){
		  $(".search-hot-words").show();});
###定时器
         function exportTimer(){
	            timer=setInterval(function(){
	              var move=$(".xm-carousel").css("margin-left");
	              if(move=="0px"){
	              	next();
	              }
	              if(move=="-1226px"){
	              	prev();
	              }
	            },4000);
			}
			exportTimer();
			$(".mprev").hover(
				function(){
					clearInterval(timer)
				},
				function(){
					exportTimer();
				}
			)
			$(".mnext").hover(
				function(){
					clearInterval(timer)
				},             
				function(){
					exportTimer();
				}
			)