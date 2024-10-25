<!-- 高血脂 -->
<template>
    <div class="body">
        <div class="header">
            <router-link :to="{ path: '/oldman/Healthyguide' }">
                <div class="return">
                    <img src="@/assets/images/return.png" alt="">
                    <div title="返回健康指导">返回</div>
                </div>
            </router-link>
        </div>
        <div class="content">
            <div class="content-video">
                <video class="video" src="@/assets/videos/Healthy2.mp4" controls></video>
            </div>
            <div class="content-text">
                <div class="Ctext-header">简介</div>
                <div class="Ctext-title">
                    高血脂
                </div>
                <div class="Ctext-content">
                    高脂血症，也称高血脂或血脂异常，通常指血浆中甘油三酯和（或）总胆固醇升高，低密度脂蛋白胆固醇升高和高密度脂蛋白胆固醇降低。该症的发生可见于不同年龄和性别的人群，尤其常见于50~69岁人群，有明显的遗传倾向。疾病的发病原因包括基因突变、多种环境因素，如不良饮食习惯、体力活动不足、肥胖等，以及其他疾病如糖尿病、肾病综合征、肝脏疾病等。
                    <br>高脂血症的典型症状包括黄色瘤、早发性角膜环、眼底改变，但在大多数情况下，症状并不明显，通常在因其他疾病就诊或常规体检时被发现。高脂血症不具有传染性。
                    <br>高脂血症的治疗主要包括生活方式干预和药物治疗。生活方式的改变包含改善饮食习惯、增加体力活动等。药物治疗主要有他汀类调脂药、贝特类调脂药、烟酸和高纯度鱼油等。如果患者同时患有重度肥胖，也可以考虑进行减重手术。积极的治疗有利于疾病的预后，但需要注意的是，高脂血症存在引发冠心病、脑血管病等并发疾病的风险。
                </div>
                <div class="Ctext-middle">相关推荐</div>
                <router-link :to="{ path: '/oldman/HguideHypertension' }">
                    <div class="content-inner">
                        <div class="Cinner-Images">
                            <img src="@/assets/images/HknowHabits1.jpg" alt="">
                        </div>
                        <div class="Cinner-text">
                            <div class="Cinner-title">高血压</div>
                            <div class="Cinner-introduce">
                                即血压升高，是血液在流动时对血管壁造成的压力值持续高于正常的现象。根据《中国高血压临床实践指南》，成人高血压的诊断标准是收缩压≥130mmHg和/或舒张压≥80mmHg。高血压的发病原因多为遗传因素和不健康的生活方式，如高盐饮食、过量饮酒、长期精神紧张和体力活动不足等。高血压在5类人群中易发：有家族史的人群；情绪易激动的人群；摄入盐量偏高的人群；嗜酒人群；工作或生活压力大的人群。
                            </div>
                        </div>
                    </div>
                </router-link>
                <router-link :to="{ path: '/oldman/HguideHypertension' }">
                    <div class="content-inner">
                        <div class="Cinner-Images">
                            <img src="@/assets/images/HknowHabits1.jpg" alt="">
                        </div>
                        <div class="Cinner-text">
                            <div class="Cinner-title">高血糖</div>
                            <div class="Cinner-introduce">
                                高血糖指的是血液中的葡萄糖含量高于正常值的范围。在临床上空腹血糖正常值为4.4~6.1mmol/L。餐后2小时血糖正常值为≤7.8
                                mmol/L。如果空腹血糖高于6.1mmol/L，餐后2小时血糖高于7.8mmol/L，均可以称为高血糖。<br>高血糖不是一种疾病的诊断，只是一种血糖监测结果的判定，高血糖不完全等于糖尿病。高血糖可能是由于遗传因素、环境因素等原因导致的。
                                一般患者可出现可有血糖升高、口渴、多饮、多尿、乏力、体重减轻等症状。长期高血糖还会导致全身微动脉血管病变，可导致相应器官损害，发生糖尿病肾病、糖尿病视网膜病变、糖尿病神经病变、糖尿病足等。高血糖没有传染性，也没有潜伏期。
                                <br>高血糖在治疗时需要针对病因治疗，一般生理性高血糖不需要特殊治疗。病理性的高血糖需要针对病因进行相应的治疗，而通常在临床上多会采取药物治疗，控制血糖正常。对于因嗜铬细胞瘤、胰高血糖素瘤等疾病引起的高血糖需要手术治疗，切出肿瘤，达到治疗的目的。
                            </div>
                        </div>
                    </div>
                </router-link>
            </div>
        </div>
    </div>
</template>

<script>

</script>

<style scoped>
.body {
    width: 100vw;
    height: 100vh;
    overflow-x: hidden;
}

/* 导航栏 */
.header {
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


.content {
    width: 100vw;
    height: 91vh;
    margin-top: 9vh;
    overflow-y: hidden;
}

/* 左边视频 */
.content .content-video {
    margin-left: 2vw;
    float: left;
}

.content .video {
    width: 66vw;
    height: 91vh;
}

/* 右边文本 */
.content .content-text {
    height: 91vh;
    background-color: #fff;
    padding: 0 1vw 0 1vw;
    margin-left: 69vw;
    margin-right: 2vw;
    border-radius: 1vh;
}

.content-text .Ctext-header {
    height: 4vh;
    border-bottom: 1px solid #ccc;
    margin-bottom: 1vh;
    font-weight: bold;
}

.content-text .Ctext-title {
    font-size: 24px;
    color: skyblue;
}

.content-text .Ctext-content {
    border-bottom: 1px solid #ccc;
    padding-bottom: 2vh;
}

.content-text .Ctext-middle {
    margin-top: 1vh;
    font-weight: bold;
}

.content-inner {
    height: 16vh;
    margin-top: 1vw;
    border-radius: 0.5vw;
}

.content-inner:hover {
    background-color: #e7e5e5;
}

.content-inner .Cinner-Images img {
    width: 12vw;
    height: 14vh;
    float: left;
    border-radius: 1vh;
    margin: 1vh 0 1vh 0.5vw;
}

.content-inner .Cinner-text {
    margin: 0 0.5vw 0 13vw;
}

.content-inner .Cinner-title {
    color: skyblue;
    font-size: 1.2vw;
    padding-top: 1vh;
    margin-bottom: 1vh;
}

.content-inner .Cinner-introduce {
    color: #666565;
    font-size: 17px;
    line-height: 24px;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    overflow: hidden;
    text-overflow: ellipsis;
    margin-top: 8px;
}

.content-inner .Cinner-introduce:hover {
    color: rgb(147, 172, 241);
}
</style>