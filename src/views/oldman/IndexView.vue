<!-- 首页 -->
<template>
    <div id="main">
        <div class="HeaderFather">
            <div class="header">
                <div id="logo">
                    <img src="@/assets/images/logo.png" alt="" style="width: 70px; max-width: 100px;">
                </div>
                <div class="logoContent">老年健康服务平台</div>
                <div class="nav-links">
                    <div class="ai"><i>AI</i>
                        答疑解惑</div>
                    <div class="nav-link"><router-link :to="{ path: '/oldman/index' }"
                            class="nav-link-inner">首页</router-link>
                    </div>
                    <div class="nav-link"><router-link :to="{ path: '/oldman/Hknowledge' }"
                            class="nav-link-inner">健康知识库</router-link></div>
                    <div class="nav-link">
                        健康指导</div>
                    <div class="nav-link">
                        智慧养老</div>
                </div>
                <div class="actions">
                    <div class="login" v-if="!isLoggedIn">
                        <router-link :to="{ path: '/oldman/Login' }" class="login-inner">
                            登录
                        </router-link>
                    </div>
                    <div class="register" v-if="!isLoggedIn">
                        <router-link :to="{ path: '/oldman/Register' }" class="register-inner">
                            免费注册
                        </router-link>
                    </div>
                    <div v-if="isLoggedIn"><img :src="userImg" @click="toggleDropdown" alt=""
                            style="width: 2vw; position: relative; left: 10vw; cursor: pointer;"></div>
                    <!-- 下拉菜单 -->
                    <div class="dropdown-menu" v-if="showDropdown">
                        <ul>
                            <!-- <li @click="userCenter" class="dropdown-item">个人中心</li> -->
                            <li @click="logout" class="dropdown-item">退出登录</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        <!-- <div class="header">
            <div class="logo">
                <img src="@/assets/images/logo.png" alt="">
            </div>
            <div class="welcomeAll">
                <div class="welcome">欢迎来到老年健康服务平台</div>
                <div class="welcome_English">
                    Welcome to the Senior Health Service Platform.
                </div>
            </div>

            <div class="actions">
                <div class="login" v-if="!isLoggedIn">
                    <router-link :to="{ path: '/oldman/Login' }" class="login-inner">
                        登录
                    </router-link>
                </div>
                <div class="register" v-if="!isLoggedIn">
                    <router-link :to="{ path: '/oldman/Register' }" class="register-inner">
                        免费注册
                    </router-link>
                </div>
                <div v-if="isLoggedIn"><img :src="userImg" @click="toggleDropdown" alt=""
                        style="width: 2vw; position: relative; left: 10vw; cursor: pointer;"></div> -->
        <!-- 下拉菜单 -->
        <!-- <div class="dropdown-menu" v-if="showDropdown">
                    <ul> -->
        <!-- <li @click="userCenter" class="dropdown-item">个人中心</li> -->
        <!-- <li @click="logout" class="dropdown-item">退出登录</li>
                    </ul>
                </div>
            </div>
        </div> -->
        <!-- <div class="middle">
            <div class="button">
                <div class="AI" @click="handClick">AI 问答</div>
                <router-link :to="{ path: '/oldman/Hknowledge' }">
                    <div class="enter">进入了解</div>
                </router-link>
            </div>
        </div> -->
        <div class="banner">
            <img :src="images[idx]" alt="">
            <div @click="prev" class="carousel-control prev"><img src="@/assets/images/next.svg" alt=""></div>
            <div @click="next" class="carousel-control next"><img src="@/assets/images/next.svg" alt=""></div>
            <div class="image-list">
                <div :style="{ 'background-color': idx == image - 1 ? '#fff' : '#525050' }"
                    v-for="(image, index) in images.length" :key="index"></div>
            </div>
        </div>

        <div class="content">
            <div class="content-left">
                <div class="title">关于我们</div>
                <div class="content-text">
                    随着科技的不断发展以及对老年群体健康生活关注度的日益提升，我们倾力打造了这款专门服务于老年人的综合性平台，旨在全方位助力老年人过上健康、便捷、舒心的生活，平台汇聚了多项实用且贴心的功能。
                    <br>AI 答疑解惑，在日常生活中，老年人常常会遇到各种各样的疑问，尤其是关乎自身健康方面的问题。而我们平台搭载的先进人工智能系统，就能成为他们随时咨询的 “健康小助手”。
                    <br>我们深知老年人对于健康知识有着多方面的需求，因此精心构建了一个涵盖生活习惯、营养饮食、运动指导、心理健康、疾病预防以及作息指南六大领域的健康知识库。
                    <br>健康指导是平台的又一核心板块，重点聚焦于疾病预防和健康运动指导这两大关键领域，致力于为老年人提供科学、专业且实用的科普知识。
                </div>
            </div>
            <div class="content-right">
                <img src="@/assets/images/1.jpg" alt="">
            </div>
        </div>

        <div class="square">
            <ul>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ul>
        </div>
        <div class="circle">
            <ul>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ul>
        </div>
        <div class="footer">
            <router-link :to="{path: '/oldman/index'}">关于我们</router-link>
            <router-link :to="{path: '/oldman/index'}">联系我们</router-link>
            <router-link :to="{path: '/oldman/index'}">官方抖音</router-link>
            <router-link :to="{path: '/oldman/index'}">加入我们</router-link>
        </div>
    </div>
</template>

<script>
/* eslint-disable */
export default {
    data() {
        return {
            images: [
                require('@/assets/images/Hknowledgebg.jpg'),
                require('@/assets/images/Hknowledgebg1.jpg'),
                require('@/assets/images/HknowRest1.jpg')
            ],
            idx: -1,
            timer: null,
            isLoggedIn: false,
            userImg: require('@/assets/images/user.png'), // 确保路径正确
            showDropdown: false, // 控制下拉框显示的状态
        }
    },
    methods: {
        handClick() {
            // 判断是否登录
            if (localStorage.getItem('token')) {
                // 如果 token 存在，则假设用户已经登录
                this.$router.replace({ path: '/oldman/Aianswer' });
            } else {
                // 如果没有 token，跳转到登录页面
                alert('请先登录');
                this.$router.replace({ path: '/oldman/Login' });
            }
        },
        checkLogin() {
            if (localStorage.getItem('token')) {
                this.isLoggedIn = true;
                this.userImg = require('@/assets/images/user.png');
            }
        },
        toggleDropdown() {
            this.showDropdown = !this.showDropdown; // 切换下拉菜单的显示状态
        },
        userCenter() {
            this.$router.replace({ path: '/Oldman/userCenter' });
        },
        logout() {
            localStorage.clear();
            this.$router.replace({ path: '/oldman/Login' });
        },
        showImages() {
            this.idx = (this.idx + 1) % this.images.length;
            this.timer = setTimeout(() => {
                this.showImages();
            }, 4500)
        },
        next() {
            this.idx =
                (this.idx + 1) % this.images.length;
        },
        prev() {
            this.idx =
                (this.idx - 1 + this.images.length) % this.images.length;
        }

    },
    created() {
        this.checkLogin(); // 在组件创建时检查登录状态
    },
    mounted() {
        this.showImages(),
            this.checkLogin();
    }
}

</script>

<style scoped>
.banner {
    width: 100%;
    height: 580px;
    position: relative;
    margin: 74px auto 0 auto;
}

.banner>img {
    width: 100%;
    height: 580px;
}

.banner .image-list {
    position: absolute;
    left: 45vw;
    bottom: 10px;
    display: flex;
    flex: row;
}

.banner .image-list div {
    width: 50px;
    height: 4px;
    margin: 10px;
    opacity: 0.7;
}
.banner .prev {
    width: 50px;
    position: absolute;
    left: 20px;
    bottom: 250px;
    cursor: pointer;
}

.banner .prev img {
    width: 50px;
}

.banner .next {
    width: 50px;
    position: absolute;
    right: 20px;
    bottom: 250px;
    cursor: pointer;
}

.banner .next img {
    width: 50px;
    transform: scaleX(-1);
}

.square ul li {
    position: relative;
    border: 1px solid #fff;
    width: 30px;
    height: 30px;
    background-color: #fff;
    list-style-type: none;
    opacity: 0;
}

.circle ul li {
    position: relative;
    border: 1px solid #fff;
    width: 30px;
    height: 30px;
    background-color: #fff;
    list-style-type: none;
    opacity: 0;
}

.square ul li {
    bottom: 4vh;
    left: 20vw;
    /* 执行动画，动画名 时长 线性的 无限次播放 */
    animation: square 10s linear infinite;
}

.square li:nth-child(2) {
    bottom: 60vh;
    left: 20vw;
    /* 设置动画延迟 */
    animation-delay: 2s;
}

.square li:nth-child(3) {
    bottom: 70vh;
    left: 76vw;
    /* 设置动画延迟 */
    animation-delay: 4s;
}

.square li:nth-child(4) {
    bottom: 10vh;
    left: 75vw;
    /* 设置动画延迟 */
    animation-delay: 6s;
}

.square li:nth-child(5) {
    bottom: 50vh;
    left: 70vw;
    /* 设置动画延迟 */
    animation-delay: 8s;
}

.circle li {
    bottom: 0;
    left: 15vw;
    /* 执行动画 */
    animation: circle 10s linear infinite;
}

.circle li:nth-child(2) {
    left: 35vw;
    /* 设置动画延迟 */
    animation-delay: 2s;
}

.circle li:nth-child(3) {
    left: 55vw;
    /* 设置动画延迟 */
    animation-delay: 6s;
}

.circle li:nth-child(4) {
    left: 75vw;
    /* 设置动画延迟 */
    animation-delay: 4s;
}

.circle li:nth-child(5) {
    left: 90vw;
    /* 设置动画延迟 */
    animation-delay: 8s;
}

/* 定义动画 */
@keyframes square {
    0% {
        transform: scale(0) rotateY(0deg);
        opacity: 1;
        bottom: 0;
        border-radius: 0;
    }

    100% {
        transform: scale(5) rotateY(1000deg);
        opacity: 0;
        bottom: 90;
        border-radius: 50%;
    }
}

@keyframes circle {
    0% {
        transform: scale(0) rotateY(0deg);
        opacity: 1;
    }

    100% {
        transform: scale(5) rotateY(1000deg);
        opacity: 0;
    }
}

.logo {
    width: 200px;
    height: 200px;
}

.logo img {
    width: 200px;
    height: 200px;
}
.img1 {
    position: relative;
    top: 100px;
    right: 800px;
}

.img1 img {
    width: 500px;
    height: 350px;
    transform: rotate(10deg);
}

.img2 {
    position: relative;
    left: 450px;
    bottom: 200px;
    /* margin-left: 20px; */

}

.img2 img {
    width: 700px;
}

.img3 {
    position: relative;
    left: 1000px;
    bottom: 700px;
}

.img3 img {
    width: 500px;
    height: 350px;
    transform: rotate(-30deg);
}

.middle {
    /* width: 1600px; */
    /* margin: 0 auto; */
    display: flex;
    justify-content: end;
}

.trigger {
    width: 30px;
    height: 90px;
    cursor: pointer;
    padding: 8px;
    background-color: #007BFF;
    color: white;
    border-radius: 5px;
    text-align: center;
}

.sidebar {
    width: 250px;
    height: 90px;
    background-color: #f8f9fa;
    position: absolute;
    top: 0;
    right: -250px;
    /* 初始位置在屏幕右侧外 */
    transition: right 0.3s ease;
    /* 添加过渡效果 */
    box-shadow: -3px 0 10px rgba(0, 0, 0, 0.1);
}

.middle .button .AI {
    width: 100px;
    height: 40px;
    line-height: 40px;
    background-color: #fff;
    text-align: center;
    float: left;
    cursor: pointer;
    color: #2280eb;
    border-radius: 4px;
}

.middle .button .enter {
    width: 100px;
    height: 40px;
    line-height: 40px;
    background-color: #fff;
    text-align: center;
    margin-left: 30px;
    float: left;
    cursor: pointer;
    color: #353535;
    border-radius: 4px;
}

.el-row {
    margin: 0 auto;

}

.welcomeAll {
    width: 1200px;
    text-align: center;
    padding-top: 70px;
}

.welcome {
    font-size: 54px;
    color: white;
    letter-spacing: 12px;
}

.welcome_English {
    font-size: 26px;
    color: white;
    letter-spacing: 2px;
}

/* 导航部分 */
.HeaderFather {
    width: 100%;
    overflow: hidden;
    border-bottom: 1px solid #aba8a8;
    position: fixed;
    z-index: 1000;
    backdrop-filter: blur(15px);
}

.header {
    width: 1500px;
    height: 74px;
    font-size: 17px;
    display: flex;
    align-items: center;
    margin: 0 auto;
}

.dropdown-menu {
    position: relative;
    top: 5vh;
    left: 6.6vw;
    width: 5vw;
    height: 5vh;
    background-color: #2280eb;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
    color: rgb(184, 208, 255);
    font-size: 16px;
    font-weight: bold;
    line-height: 5vh;
    /* padding-top: 0.5vh; */
    text-align: center;

    z-index: 1;
}

.dropdown-menu ul {
    list-style: none;
    padding: 0;
    margin: 0;
    /* color: #868282; */
}

.dropdown-item {
    /* padding: 12px 16px; */
    cursor: pointer;
    transition: background-color 0.3s;
    /* color: #868282; */
    /* 添加平滑过渡效果 */
}

.dropdown-item:hover {
    background-color: #8292ff;
    /* 鼠标悬停时的背景色 */
}

.logoContent {
    font-size: 25px;
    font-weight: bold;
}

#logo {
    margin-left: 20px;
}

.nav-links {
    display: flex;
    align-items: center;
    margin-left: 150px;
}

.header .nav-links .ai {
    width: 104px;
    height: 50px;
    line-height: 50px;
    text-align: center;
    border-radius: 10px;
    background-color: #798bf0;
    float: left;
    color: #fffffffb;
    cursor: pointer;
}

.header .nav-links .ai .ai-inner {
    display: block;
    /* 使router-link充满整个父div */
    width: 100%;
    height: 100%;
    color: inherit;
}

.header .nav-links .ai:hover {
    background-image: linear-gradient(to bottom right, rgb(104, 106, 237), rgb(97, 82, 236), rgb(52, 58, 232));
}

.header .nav-links .nav-link {
    width: 130px;
    height: 70px;
    line-height: 70px;
    text-align: center;
    color: #8a5b8e;
    margin-left: 15px;
    cursor: pointer;
}

.nav-link-inner,
.ai-inner,
.login-inner,
.register-inner,
.understand-inner {
    display: block;
    /* 使router-link充满整个父div */
    width: 100%;
    height: 100%;
    color: inherit;
}

.header .nav-links .nav-link:hover {
    border-bottom: 6px solid rgb(161, 82, 236);
    color: rgb(161, 82, 236);
}

.header .nav-links .nav-link:nth-child(2) {
    border-bottom: 6px solid rgb(161, 82, 236);
    color: rgb(161, 82, 236);
}

.actions {
    display: flex;
    color: #8a5b8e;
    align-items: center;
    margin-left: 140px;
}

.header .actions .login {
    width: 68px;
    height: 41px;
    line-height: 41px;
    text-align: center;
    border: 1px solid #868282;
    margin-left: 10px;
    border-radius: 28px;
    cursor: pointer;
}

.header .actions .login:hover {
    border: 1px solid #da44eb;
    color: #da44eb;
}

.header .actions .register {
    width: 102px;
    height: 41px;
    line-height: 41px;
    text-align: center;
    background-color: #e334ed;
    margin-left: 16px;
    border-radius: 28px;
    color: #fff;
    cursor: pointer;
}

.header .actions .register:hover {
    background-image: linear-gradient(to bottom right, rgb(195, 54, 220), rgb(207, 55, 207), rgb(197, 31, 174));
}

.content {
    width: 1200px;
    margin: 100px auto 0 auto;
    display: flex;
}

.content .content-left {
    width: 600px;
    padding-right: 50px;
}

.content .content-left .title {
    font-size: 28px;
}

.content .content-left .content-text {
    margin-top: 50px;
    font-size: 20px;
    line-height: 50px;
    color: rgba(119, 119, 119, 1);
}

.content .content-right {
    width: 600px;
    margin-top: 100px;
}

.content .content-right img {
    width: 600px;
}
.footer {
    width: 1200px;
    height: 120px;
    line-height: 80px;
    text-align: center;
    border-top: 1px solid #ccc;
    margin: 0 auto;
}
.footer a{
    margin: 20px 40px;
    color: rgba(119, 119, 119, 1);

}
.footer a:hover{
    color: blue;
}
#main {
    position: relative;
    border-radius: 10px;
    width: 100vw;
    height: 100vh;
    overflow-x: hidden;
    /* background-color: #afd0ff; */
    /* background-image: linear-gradient(to bottom right, rgb(206, 240, 180), rgb(187, 231, 244), rgb(135, 235, 156)); */
}</style>