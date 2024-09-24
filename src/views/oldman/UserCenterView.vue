<!-- 个人中心 -->
<template>
    <div class="body">
        <!-- 导航栏 -->
        <div class="nav_header">
            <img src="img/logo.png" alt="">
            <span class="span1">oldman_healthy</span>
        </div>
        <!-- 中间部分--基本资料 -->
        <div class="nav_body">
            <div class="nav_body_font">基本资料</div>
            <div class="nav_body_body">
                <span>昵称: <input type="text" style="border-color: aliceblue; width: 20vw;"></span><br>
                <span>年龄: <input type="text" style="border-color: aliceblue; width: 20vw;"></span><br>
                <span>性别: <input id="man" type="radio" checked="checked" name="1" />男<input id="woman" type="radio"
                        name="1" />女</span><br>
                <button>保存</button>
            </div>
        </div>
        <!-- 侧边头像 -->
        <div class="left_nav_img">
            <img src="img/robot.png" alt="">
        </div>
        <div class="left_nav_name">智韵天成</div>
        <div class="left_nav">
            <span><a href="#" style="text-decoration: none;">基本资料</a></span>
            <br>
            <span><a href="#" style="text-decoration: none;">头像设置</a></span>
            <br>
            <span><a href="#" style="text-decoration: none;">修改密码</a></span>
            <br>
            <span><a href="#" style="text-decoration: none;">我的收藏</a></span>
        </div>
    </div>
</template>
<script></script>
<style>
* {
    margin: 0;
    padding: 0;
}

.nav_header {
    width: 100%;
    height: 9vh;
    background-color: rgb(245, 241, 241);

}

.nav_header img {
    width: 4vw;
    height: 4vw;
    position: relative;
    left: 10vw;
}

.span1 {
    position: relative;
    left: 4.5vw;
    top: 1vh;
    font-size: 13px;
}

.span2 {
    position: relative;
    left: 23vw;
    bottom: 1vh;
    font-size: 20px;
    font-family: "宋体";
    font-weight: bold;
}

.span3 {
    position: relative;
    left: 28vw;
    bottom: 1vh;
    font-size: 20px;
    font-family: "宋体";
    font-weight: bold;
}

.span4 {
    position: relative;
    left: 33vw;
    bottom: 1vh;
    font-size: 20px;
    font-family: "宋体";
    font-weight: bold;
}

.body {
    background-color: rgb(232, 232, 232);
    width: 100%;
    height: 100vh;
}

.left_nav_img {
    width: 10vw;
    height: 10vw;
    position: relative;
    left: 10vw;
    top: 6vh;
    background-color: aliceblue;
    border-radius: 50%;
    z-index: 2;
}

.left_nav_img img {
    width: 10vw;
    height: 10vw;
    z-index: 2;
}

.left_nav_name {
    position: relative;
    left: 9vw;
    top: 8vh;
    /* background-color: antiquewhite; */
    width: 12vw;
    text-align: center;
    z-index: 2;
}

.left_nav {
    width: 14vw;
    height: 60vh;
    background-color: white;
    position: relative;
    bottom: 2vh;
    left: 8vw;
    border-radius: 8px;
    z-index: 1;
}

.left_nav span {
    font-size: 20px;
    font-family: "宋体";
    font-weight: bold;
    position: relative;
    top: 15vh;
    left: 4vw;
    display: block;
    margin-bottom: 4vh;
}

.nav_body {
    width: 60vw;
    height: 75vh;
    background-color: white;
    position: relative;
    top: 5vh;
    right: 15vw;
    float: right;
    border-radius: 10px;
}

.nav_body_font {
    position: relative;
    left: 5vw;
    top: 3vh;
    width: 5vw;
    /* background-color: aliceblue; */
}

.nav_body_body {
    /* background-color: antiquewhite; */
    width: 50vw;
    height: 50vh;
    position: relative;
    left: 10vw;
    top: 10vh;
}

.nav_body_body span {
    font-size: 20px;
    font-family: "宋体";
    font-weight: bold;
    position: relative;
    display: block;
}

.nav_body_body button {
    font-size: 20px;
    background-color: rgb(92, 173, 255);
    width: 20vw;
    position: relative;
    left: 6vw;
    border-color: aliceblue;
}
</style>