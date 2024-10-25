<!-- 健康指导 -->
<template>
    <div class="body">
        <!-- <div class="header">
            <router-link :to="{ path: '/oldman/index' }">
                <div class="return">
                    <img src="@/assets/images/return.png" alt="">
                    <div title="首页">返回</div>
                </div>
            </router-link>
            <div class="header-logo">
                <img src="@/assets/images/logo.png" alt="" style="width: 4vw; max-width: 100px;">
            </div>
            <div class="header-title">老年健康服务平台</div>
            <router-link :to="{ path: '/oldman/userCenter' }">
                <div class="header-user">
                    <div>个人中心</div>
                    <img src="@/assets/images/user.png" alt="">
                </div>
            </router-link>
        </div> -->

        <div class="HeaderFather">
            <div class="header">
                <div id="logo">
                    <img src="@/assets/images/logo.png" alt="" style="width: 70px; max-width: 100px;">
                </div>
                <div class="logoContent">老年健康服务平台</div>
                <div class="nav-links">
                    <div class="ai"><router-link :to="{ path: '/Oldman/Aianswer' }" class="ai-inner"><i>AI</i>
                            答疑解惑</router-link></div>
                    <div class="nav-link"><router-link :to="{ path: '/oldman/index' }"
                            class="nav-link-inner">首页</router-link>
                    </div>
                    <div class="nav-link"><router-link :to="{ path: '/oldman/Hknowledge' }"
                            class="nav-link-inner">健康知识库</router-link></div>
                    <div class="nav-link"><router-link :to="{ path: '/oldman/Healthyguide' }"
                            class="nav-link-inner">健康指导</router-link></div>
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
                            style="width: 2px; position: relative; left: 10px; cursor: pointer;"></div>
                    <!-- 下拉菜单 -->
                    <div class="dropdown-menu" v-if="showDropdown">
                        <ul>
                            <li @click="userCenter" class="dropdown-item">个人中心</li>
                            <li @click="logout" class="dropdown-item">退出登录</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <div class="content">
            <div class="content-title">
                健康指导
            </div>
            <ul>
                <li>
                    <router-link :to="{ path: '/oldman/HguideHypertension' }">
                        <div class="content-inner">
                            <img src="@/assets/images/HknowHabits1.jpg" alt="">
                            <div class="Cinner-text">
                                <div class="Cinner-title">高血压</div>
                                <div class="Cinner-introduce">
                                    即血压升高，是血液在流动时对血管壁造成的压力值持续高于正常的现象。根据《中国高血压临床实践指南》，成人高血压的诊断标准是收缩压≥130mmHg和/或舒张压≥80mmHg。高血压的发病原因多为遗传因素和不健康的生活方式，如高盐饮食、过量饮酒、长期精神紧张和体力活动不足等。高血压在5类人群中易发：有家族史的人群；情绪易激动的人群；摄入盐量偏高的人群；嗜酒人群；工作或生活压力大的人群。
                                    高血压的典型症状包括头痛、疲倦或不安、心律失常、心悸耳鸣等。然而，许多高血压患者可能在没有任何症状的情况下已出现其他并发症，如脑卒中、视物模糊、意识丧失、失忆等，所以高血压被称为“无声的杀手”。
                                    对于高血压患者，改善生活方式和药物治疗是最常用的治疗方式。药物治疗的基本原则包括优先使用长效降压药物，控制24小时血压，并适时根据需要调整药物与剂量。如果高血压患者的血压长期得不到控制，可能会导致更严重的并发症，甚至可能导致卒中、脑梗死等致命的结果。
                                </div>
                            </div>
                        </div>
                    </router-link>
                </li>
                <li>
                    <router-link :to="{ path: '/oldman/HguideHyperlipidemia' }">
                        <div class="content-inner">
                            <img src="@/assets/images/HknowHealthyEat6.jpg" alt="">
                            <div class="Cinner-text">
                                <div class="Cinner-title">高血脂</div>
                                <div class="Cinner-introduce">
                                    高脂血症，也称高血脂或血脂异常，通常指血浆中甘油三酯和（或）总胆固醇升高，低密度脂蛋白胆固醇升高和高密度脂蛋白胆固醇降低。该症的发生可见于不同年龄和性别的人群，尤其常见于50~69岁人群，有明显的遗传倾向。疾病的发病原因包括基因突变、多种环境因素，如不良饮食习惯、体力活动不足、肥胖等，以及其他疾病如糖尿病、肾病综合征、肝脏疾病等。
                                    高脂血症的典型症状包括黄色瘤、早发性角膜环、眼底改变，但在大多数情况下，症状并不明显，通常在因其他疾病就诊或常规体检时被发现。高脂血症不具有传染性。
                                    高脂血症的治疗主要包括生活方式干预和药物治疗。生活方式的改变包含改善饮食习惯、增加体力活动等。药物治疗主要有他汀类调脂药、贝特类调脂药、烟酸和高纯度鱼油等。如果患者同时患有重度肥胖，也可以考虑进行减重手术。积极的治疗有利于疾病的预后，但需要注意的是，高脂血症存在引发冠心病、脑血管病等并发疾病的风险。
                                </div>
                            </div>
                        </div>
                    </router-link>
                </li>
                <li>
                    <router-link :to="{ path: '/oldman/HguideHyperglycemia' }">
                        <div class="content-inner">
                            <img src="@/assets/images/HknowSportInstruction2.jpg" alt="">
                            <div class="Cinner-text">
                                <div class="Cinner-title">高血糖</div>
                                <div class="Cinner-introduce">
                                    高血糖指的是血液中的葡萄糖含量高于正常值的范围。在临床上空腹血糖正常值为4.4~6.1mmol/L。餐后2小时血糖正常值为≤7.8
                                    mmol/L。如果空腹血糖高于6.1mmol/L，餐后2小时血糖高于7.8mmol/L，均可以称为高血糖。<br>高血糖不是一种疾病的诊断，只是一种血糖监测结果的判定，高血糖不完全等于糖尿病。高血糖可能是由于遗传因素、环境因素等原因导致的。
                                    一般患者可出现可有血糖升高、口渴、多饮、多尿、乏力、体重减轻等症状。长期高血糖还会导致全身微动脉血管病变，可导致相应器官损害，发生糖尿病肾病、糖尿病视网膜病变、糖尿病神经病变、糖尿病足等。高血糖没有传染性，也没有潜伏期。
                                    高血糖在治疗时需要针对病因治疗，一般生理性高血糖不需要特殊治疗。病理性的高血糖需要针对病因进行相应的治疗，而通常在临床上多会采取药物治疗，控制血糖正常。对于因嗜铬细胞瘤、胰高血糖素瘤等疾病引起的高血糖需要手术治疗，切出肿瘤，达到治疗的目的。
                                </div>
                            </div>
                        </div>
                    </router-link>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
// const DiseaseOptions = [];
// export default {
//     data() {
//         return {
//             checkAll: false,
//             checkedDiseases: [],
//             Diseases: DiseaseOptions,
//             isIndeterminate: true
//         };
//     },
//     methods: {
//         handleCheckAllChange(val) {
//             this.checkedCities = val ? DiseaseOptions : [];
//             this.isIndeterminate = false;
//         },
//         handleCheckedCitiesChange(value) {
//             let checkedCount = value.length;
//             this.checkAll = checkedCount === this.cities.length;
//             this.isIndeterminate = checkedCount > 0 && checkedCount < this.cities.length;
//         }
//     }
// };

export default {
    data() {
        return {
            isLoggedIn: false,
            userImg: require('@/assets/images/user.png'), // 确保路径正确
            showDropdown: false, // 控制下拉框显示的状态
        }
    },
    methods: {
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
        }

    },
    created() {
        this.checkLogin(); // 在组件创建时检查登录状态
    }
}


</script>

<style scoped>
.body {
    width: 100vw;
    height: 100vh;
    overflow-x: hidden;
    background-color: #d8e5f7;
}

/* 导航栏 */
/* .header {
    width: 100vw;
    height: 9vh;
    background: #fff;
    display: flex;
    align-items: center;
    position: fixed;
    z-index: 1000;
}

.header .return {
    width: 5vw;
    display: flex;
    align-items: center;
    margin-left: 1vw;
    font-size: 1vw;
    color: #666565;
}

.header .return:hover {
    color: rgb(161, 82, 236);

}

.header .return img {
    width: 1vw;
}

.header-logo {
    margin-left: 1vw;
}

.header-title {
    font-size: 1.5vw;
    font-weight: bold;
}

.header-user {
    margin-left: 62vw;
    font-size: 1.2vw;
    display: flex;
    align-items: center;
    color: #000;
}

.header-user>div {
    padding-right: 0.5vw;
}

.header-user img {
    width: 2vw;
} */
.HeaderFather {
    width: 100%;
    overflow: hidden;
    border-bottom: 1px solid #aba8a8;
    background-color: #fff;
}

.header {
    width: 1500px;
    height: 74px;
    font-size: 17px;
    display: flex;
    align-items: center;
    /* border-bottom: 1px solid #716565; */
    background-color: #fff;
    /* position: fixed; */
    z-index: 1000;
    margin: 0 auto;
}

.dropdown-menu {
    position: relative;
    top: 9px;
    left: 6.6px;
    width: 5px;
    height: 10px;
    background-color: #d6e7fb;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
    color: white;
    font-size: 16px;
    font-weight: bold;
    line-height: 5px;
    padding-top: 1px;
    text-align: center;

    z-index: 1;
}

.dropdown-menu ul {
    list-style: none;
    padding: 0;
    margin: 0;
}

.dropdown-item {
    /* padding: 12px 16px; */
    cursor: pointer;
    transition: background-color 0.3s;
    /* 添加平滑过渡效果 */
}

.dropdown-item:hover {
    background-color: #f1f1f1;
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
    margin-left: 200px;
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

.header .nav-links .nav-link:nth-child(4) {
    border-bottom: 6px solid rgb(161, 82, 236);
    color: rgb(161, 82, 236);
}

.actions {
    display: flex;
    color: #8a5b8e;
    align-items: center;
    margin-left: 240px;
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


/* 内容区域 */
.content {
    width: 1500px;
    border-radius: 10px;
    background-color: #fff;
    margin: 20px auto;
}

.content .content-title {
    height: 50px;
    padding-top: 25px;
    margin-left: 50px;
    font-size: 26px;
}

ul {
    padding-bottom: 20px;
}

ul li {
    width: 1400px;
    border: 1px solid #ccc;
    border-radius: 20px;
    box-sizing: border-box;
    margin: 20px auto;
    background: #fff;
}



ul li:hover {
    background-color: #f5f5f5;
}

.content-inner {
    width: 1300px;
    height: 220px;
    padding: 18px;
}

.content-inner img {
    width: 390px;
    height: 220px;
    border-radius: 10px;
    float: left;
}

.content-inner .Cinner-text {
    width: 900px;
    margin: 0 420px;
}

.content-inner .Cinner-title {
    color: skyblue;
    font-size: 26px;
}

.content-inner .Cinner-introduce {
    color: #666565;
    font-size: 17px;
    line-height: 24px;
    display: -webkit-box;
    -webkit-line-clamp: 5;
    -webkit-box-orient: vertical;
    overflow: hidden;
    text-overflow: ellipsis;
    margin-top: 16px;
}
.content-inner .Cinner-introduce:hover{
    color: rgb(147, 172, 241);
}

/* 媒体查询 */
@media screen and (max-width: 950px) {

    /* 导航栏变化 */
    .header {
        width: 950px;
        height: 74px;
        font-size: 17px;
        display: flex;
        align-items: center;
        /* border-bottom: 1px solid #716565; */
        background-color: #fff;
        /* position: fixed; */
        z-index: 1000;
        margin: 0 auto;
    }

    #logo,
    .logoContent {
        display: none;
    }


    /* 内容区域变化 */
    .content {
        width: 950px;
        border-radius: 10px;
        background-color: #fff;
        margin: 20px auto;
    }

    .content .content-title {
        height: 50px;
        padding-top: 25px;
        margin-left: 26px;
        font-size: 26px;
    }

    ul li {
        width: 900px;
        border: 1px solid #ccc;
        border-radius: 20px;
        box-sizing: border-box;
        margin: 20px auto;
    }

    ul li:hover {
        background-color: #f5f5f5;
    }

    .content-inner {
        width: 800px;
        height: 170px;
        padding: 18px;
    }

    .content-inner img {
        width: 280px;
        height: 170px;
        border-radius: 10px;
        float: left;
    }

    .content-inner .Cinner-text {
        width: 560px;
        margin: 0 300px;
    }
}
</style>