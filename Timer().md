 **自动轮播**
     
         function exportTimer(){
                timer =setInterval(function(){
                    goleft();
                },2000);
            }
            //第一次执行定时器
            exportTimer();

            $(".imgpage .prev").hover(
               function(){
                clearInterval(timer) //移除定时器
               },
               function(){
                exportTimer(); 
               }
            )
             $(".imgpage .next").hover(
               function(){
                clearInterval(timer)
               },
               function(){
                exportTimer();
               }
            )