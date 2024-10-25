<!-- 高血糖 -->
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
            <div class=" content-video">
                <video class="video" src="@/assets/videos/Healthy2.mp4" controls></video>

            </div>

            <div class="content-text">
                <div class="Ctext-header">简介</div>
                <div class="Ctext-title">
                    高血糖
                </div>
                <div class="Ctext-content">
                    高血糖指的是血液中的葡萄糖含量高于正常值的范围。在临床上空腹血糖正常值为4.4~6.1mmol/L。餐后2小时血糖正常值为≤7.8
                    mmol/L。如果空腹血糖高于6.1mmol/L，餐后2小时血糖高于7.8mmol/L，均可以称为高血糖。<br>高血糖不是一种疾病的诊断，只是一种血糖监测结果的判定，高血糖不完全等于糖尿病。高血糖可能是由于遗传因素、环境因素等原因导致的。
                    一般患者可出现可有血糖升高、口渴、多饮、多尿、乏力、体重减轻等症状。长期高血糖还会导致全身微动脉血管病变，可导致相应器官损害，发生糖尿病肾病、糖尿病视网膜病变、糖尿病神经病变、糖尿病足等。高血糖没有传染性，也没有潜伏期。
                    <br>高血糖在治疗时需要针对病因治疗，一般生理性高血糖不需要特殊治疗。病理性的高血糖需要针对病因进行相应的治疗，而通常在临床上多会采取药物治疗，控制血糖正常。对于因嗜铬细胞瘤、胰高血糖素瘤等疾病引起的高血糖需要手术治疗，切出肿瘤，达到治疗的目的。
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
                                <br>高血压的典型症状包括头痛、疲倦或不安、心律失常、心悸耳鸣等。然而，许多高血压患者可能在没有任何症状的情况下已出现其他并发症，如脑卒中、视物模糊、意识丧失、失忆等，所以高血压被称为“无声的杀手”。
                                <br>对于高血压患者，改善生活方式和药物治疗是最常用的治疗方式。药物治疗的基本原则包括优先使用长效降压药物，控制24小时血压，并适时根据需要调整药物与剂量。如果高血压患者的血压长期得不到控制，可能会导致更严重的并发症，甚至可能导致卒中、脑梗死等致命的结果。
                            </div>
                        </div>
                    </div>
                </router-link>
                <router-link :to="{ path: '/oldman/HguideHyperlipidemia' }">
                    <div class="content-inner">
                        <div class="Cinner-Images">
                            <img src="@/assets/images/HknowHabits1.jpg" alt="">
                        </div>
                        <div class="Cinner-text">
                            <div class="Cinner-title">高血脂</div>
                            <div class="Cinner-introduce">
                                高脂血症，也称高血脂或血脂异常，通常指血浆中甘油三酯和（或）总胆固醇升高，低密度脂蛋白胆固醇升高和高密度脂蛋白胆固醇降低。该症的发生可见于不同年龄和性别的人群，尤其常见于50~69岁人群，有明显的遗传倾向。疾病的发病原因包括基因突变、多种环境因素，如不良饮食习惯、体力活动不足、肥胖等，以及其他疾病如糖尿病、肾病综合征、肝脏疾病等。
                                <br>高脂血症的典型症状包括黄色瘤、早发性角膜环、眼底改变，但在大多数情况下，症状并不明显，通常在因其他疾病就诊或常规体检时被发现。高脂血症不具有传染性。
                                <br>高脂血症的治疗主要包括生活方式干预和药物治疗。生活方式的改变包含改善饮食习惯、增加体力活动等。药物治疗主要有他汀类调脂药、贝特类调脂药、烟酸和高纯度鱼油等。如果患者同时患有重度肥胖，也可以考虑进行减重手术。积极的治疗有利于疾病的预后，但需要注意的是，高脂血症存在引发冠心病、脑血管病等并发疾病的风险。
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
    width: 100%;
    overflow: hidden;
}

/* 导航栏 */
.header {
    width: 100%;
    height: 70px;
    line-height: 70px;
    background: #fff;
    /* background-color: burlywood; */
}

.header .return {
    width: 60px;
    display: flex;
    align-items: center;
    margin-left: 70px;
    font-size: 18px;
    color: #666565;
}

.header .return:hover {
    color: rgb(161, 82, 236);

}

.header .return img {
    width: 18px;
}

/* 内容区域 */
.content {
    width: 100%;
    height: 755px;
    overflow: hidden;

}

/* 左边视频 */
.content .content-video {
    width: 1130px;
    margin-left: 70px;
    float: left;
}

.content .video {
    width: 1130px;
}

/* 右边文本 */
.content .content-text {
    width: 430px;
    background-color: #fff;
    padding: 0 14px;
    margin-left: 1200px;
    margin-right: 90px;
    border-radius: 10px;
}

.content-text .Ctext-header {
    height: 35px;
    border-bottom: 1px solid #ccc;
    margin-bottom: 18px;
    font-weight: bold;
}

.content-text .Ctext-title {
    font-size: 24px;
    color: skyblue;
}

.content-text .Ctext-content {
    border-bottom: 1px solid #ccc;
    padding-bottom: 30px;
    overflow-y: auto;
    /* 或者使用 scroll，但 auto 会在必要时才显示滚动条 */
    height: 300px;
}

.content-text .Ctext-content::-webkit-scrollbar {
    display: none;
}

.content-text .Ctext-middle {
    margin-top: 20px;
    font-weight: bold;
}

.content-inner {
    height: 130px;
    margin-top: 14px;
    border-radius: 8px;
}

.content-inner:hover {
    background-color: #e7e5e5;
}

.content-inner .Cinner-Images img {
    width: 200px;
    height: 110px;
    float: left;
    border-radius: 10px;
    margin: 10px 0 10px 10px;
}

.content-inner .Cinner-text {
    margin: 0 10px 0 220px;
}

.content-inner .Cinner-title {
    color: skyblue;
    font-size: 20px;
    padding-top: 10px;
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

@media screen and (max-width: 1500px) {
    .header {
        width: 100%;
        height: 50px;
        line-height: 50px;
    }

    .header .return {
        margin-left: 50px;
    }

    .content .content-video {
        width: 1000px;
        margin-left: 50px;
        float: left;
    }

    .content .video {
        width: 1050px;
    }

    .content .content-text {
        width: 340px;
        background-color: #fff;
        padding: 0 14px;
        margin-left: 1100px;
        margin-right: 50px;
        border-radius: 10px;
    }

    .content-text .Ctext-content {
        height: 260px;
    }

}
</style>