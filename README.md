# snake
Canvas snake game

$(function(){
    // 贪吃蛇初始化
    if($("html").hasClass("canvas")){
        // 当浏览器支持canvas时，载入游戏js，并初始化游戏            
        $("head").linkAdd(['http://img1.tiancitycdn.com/project5/csol2/event/2016/1205event/js/jquery.snakeGame.min.js'],function(){
                // js加载成功后启动游戏
                var _snake = $(".game-stage").snakeGame({
                    beforeStart : function(){
                        // return false; 不启动游戏
                        return true;
                    },
                    onGameover : function(score,deadMode){
                        // 游戏结束弹窗
                        alert("游戏结束！您的得分为："+score);
                    }
                });
        });
    }
});