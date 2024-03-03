<template>
    <div class="home" @touchstart="arrow_up = true">
        <div class="header">

            <div class="bilingual" @touchstart.stop="checkArrow">
                <span class="language">{{ language[selectLanguageIndex - 1] }}</span>
                <span class="rtbg"></span>
                <span :class="['arrow_down', { arrow_up: !arrow_up }]"></span>
                <div :class="['check', { check_show: !arrow_up }]">
                    <span @touchstart.stop="changeLaguage(index + 1)" v-for="(item, index) in language" :key="index">{{ item
                    }}</span>
                </div>
            </div>

            <div class="title_3">
                <div class="date_t">
                    <div class="s_t">
                        <span>21/8</span>
                    </div>
                    <div class="line">-</div>
                    <div class="s_t">
                        <span>30/8</span>
                    </div>
                </div>
            </div>

            <!-- ruleBtn -->
            <div class="float_rules" @click="openRule">
                <span :class="selectLanguageIndex == 5 ? ' mgaText' : ''">
                    {{ btnTextList[selectLanguageIndex - 1] }}</span>
            </div>
            <!-- curt_timer -->
            <div class="curt_timer">
                <ul>
                    <li>
                        <div class="time">{{ timer.days }}</div>
                    </li>

                    <li>
                        <div class="time">D</div>
                    </li>
                    <li>
                        <div class="time">{{ timer.hours }}</div>
                    </li>
                    <span> : </span>
                    <li>
                        <div class="time">{{ timer.mins }}</div>
                    </li>
                    <span> :</span>
                    <li>
                        <div class="time">{{ timer.secs }}</div>
                    </li>
                </ul>
            </div>
        </div>

        <!-- howtoplay -->
        <howtoplay :language="selectLanguageIndex" v-if="ruleShow" @closeMe="ruleShow = false"></howtoplay>
        <!-- <leaderBoardComp /> -->
    </div>
</template>
<script>
import { ref } from "vue";
import howtoplay from "./howToPlay.vue";
// import leaderBoardComp from "./leaderBoardComp.vue";

export default {
    components: {
        howtoplay,
        // leaderBoardComp
    },
    setup() {
        let canClick = ref(true);
        let timer = ref({ days: "00", hours: "00", mins: "00", secs: "00" });
        let userAmount = ref(0);
        let rewardPopShow = ref(false); //
        let showRewardList = ref(null); //
        let arrow_up = ref(true);
        let ruleShow = ref(false);
        let activeSwitch = ref(0);
        let selectLanguageIndex = ref(1);
        let activeKey = ref("");
        let activeEnd = ref(false);
        let rankingRules = ref([]);
        let periodKey = ref("");
        let rewardShow = ref(false);
        let rewardList = ref();
        let errorPageshow = ref(false);
        let errorPageStatus = ref(0);
        let language = ref(["English", "Urdu", "Hindi", "Bengali", "Filipino"]);
        let btnTextList = ref(["Rules", "قواعد", "नियम", "নিয়ম", "Mga tuntunin"]);
        let mountList = ref([]);

        let luckyRewardList = ref([]);
        function changeLaguage(type) {
            arrow_up.value = true;
            selectLanguageIndex.value = type;
            baseFun("language");
        }
        function checkArrow() {
            arrow_up.value = !arrow_up.value;
        }

        function openRule() {
            ruleShow.value = true;
            baseFun("rule");
        }

        function baseFun(location) {
            const lang = language.value[selectLanguageIndex.value - 1];
            // Assuming window.oyetalkActivityJsAnalysis is initialized somewhere else
            if (window.oyetalkActivityJsAnalysis && window.oyetalkActivityJsAnalysis.track) {
                window.oyetalkActivityJsAnalysis.track("click_event", {
                    location,
                    module: window.location.href.split("?")[0],
                    name: activeKey.value,
                    language: lang,
                });
            }
        }


        return {
            luckyRewardList,
            mountList,
            activeEnd,
            canClick,
            userAmount,
            errorPageshow,
            errorPageStatus,
            showRewardList,
            rewardPopShow,
            rewardList,
            rewardShow,
            activeSwitch,
            periodKey,
            openRule,
            timer,
            arrow_up,
            ruleShow,
            language,
            btnTextList,
            selectLanguageIndex,
            checkArrow,
            changeLaguage,
            rankingRules,
        };
    },
};
</script>
<style lang="less" scoped>
.home {
    width: 100%;

    .bgc {
        position: relative;
        // padding-top: 18px;
        background: linear-gradient(180deg, #917af4, #6d50e8);
    }

    .bgImg {
        width: 375px;
        height: 315px;
        // background: url("../assets/img/background_leaderboard.png") no-repeat;
        background-size: 100% 100%;
        position: absolute;
        left: 50%;
        top: 960px;
        transform: translateX(-50%);
    }

    .grayFilt {
        filter: grayscale(1);
    }

    .header {
        width: 100%;
        height: 300px;
        background: url("../assets/images/header.jpg") no-repeat;
        background-size: 100%;
        position: relative;

        .title_3 {
            position: absolute;
            z-index: 1;
            padding: 4px 5px;
            left: 50%;
            background-color: rgba(89, 7, 173, 0.5);
            transform: translateX(-50%);
            border-radius: 9999px;
            top: 27.4%;
            text-align: center;
            background-size: 100% 100%;
            color: #FFFDAE;

            .date_t {
                position: relative;
                display: flex;
                align-items: center;

                .s_t {
                    display: flex;
                    align-items: flex-start;

                    .b_text {
                        font-size: 11px;
                        margin-left: 1px;
                        margin-top: -1px;
                    }

                    span {
                        font-size: 11px;
                    }
                }

                .line {
                    margin: 0 6px;
                }

                .m_text {
                    margin-left: 5px;
                    font-size: 14px;
                }
            }
        }

        .bilingual {
            position: absolute;
            width: 56px;
            background-color: #fff;
            border: 2px solid rgba(193, 104, 255, 1);
            right: 5px;
            top: 10px;
            padding: 4px;
            border-radius: 9999px;
            text-align: center;
            padding-right: 20px;
            transform: scale(0.9);
            z-index: 40;

            .language {
                color: #000;
                font-size: 12px;
            }

            .rtbg {
                position: absolute;
                width: 21px;
                height: 26px;
                right: 0px;
                top: 0px;
                background: #dddd0b;
                border-top-right-radius: 2em;
                border-bottom-right-radius: 2em;
            }

            .arrow_down {
                position: absolute;
                right: 0.11rem;
                top: 0.17rem;
                cursor: pointer;
                transition-duration: 0.2s;
                width: 0;
                height: 0;
                border-width: 0.2rem 0.2rem 0;
                border-style: solid;
                border-color: #fff transparent transparent;
            }

            .arrow_up {
                transform: rotate(180deg);
                top: 0.14rem;
            }

            .check {
                width: 2.2rem;
                left: 0;
                bottom: 0;
                position: absolute;
                background-color: rgba(255, 255, 255, 0.8);
                height: 0;
                overflow: hidden;
                transition-duration: 0.2s;
                border-radius: 0.1rem;
                z-index: 15;

                span {
                    display: block;
                    width: 100%;
                    height: 0.64rem;
                    font-size: 0.24rem;
                    text-align: center;
                    line-height: 0.64rem;
                    border-bottom: 1px solid #fff;
                    color: #000;
                }

                span:last-child {
                    border-bottom: none;
                    box-sizing: border-box;
                }
            }

            .check_show {
                height: 3.3rem;
                bottom: -3.34rem;
                z-index: 15;
            }
        }
    }

    .feedback {
        position: absolute;
        z-index: 11;
        width: 38px;
        height: auto;
        right: 10px;
        top: 231px;

        img {
            width: 100%;
            height: 100%;
        }
    }

    .rewardBtn {
        width: 38px;
        height: 38px;
        // background: url("../assets/img/button_rewards.png") no-repeat;
        background-size: 100% 100%;
        right: 10px;
        top: 283px;
        position: absolute;
        z-index: 5;
    }

    .float_rules {
        position: absolute;
        background: #dddd0b;

        border: 2px solid #c4a1ff;
        border-radius: 9999px 0 0 9999px;
        width: 65px;
        height: 30px;
        font-size: 13px;
        z-index: 11;
        box-sizing: border-box;
        text-align: center;
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        right: 0;
        top: 269px;

        span {
            color: #fff;
            font-size: 13px;
        }

        background-size: 100% 100%;

        .mgaText {
            transform: scale(0.7);
            font-size: 13px;
        }
    }

    .curt_timer {
        width: 100%;
        position: absolute;
        bottom: -1rem;

        ul {
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: 400;
            color: #000;

            li {
                flex-shrink: 0;
                width: 23px;
                height: 23px;
                background-repeat: no-repeat;
                margin-right: 2px;
                display: flex;
                align-items: center;
                flex-direction: column;
                justify-content: center;
                font-weight: 400;
                box-sizing: border-box;
                background: linear-gradient(180deg, #e861ff, #b950f0);
                border: 1px solid #fff1a2;
                border-radius: 5px;

                .time {
                    vertical-align: middle;
                    font-size: 13px;
                    text-align: center;
                    font-family: "Roboto-Regular";
                    font-weight: 500;
                    color: #fff;
                }
            }

            span {
                color: #fff;
                margin-right: 2px;
                display: inline-block;
            }

            :nth-child(2) {
                margin-right: 7px;
            }
        }
    }

    .luckyText {
        position: absolute;
        bottom: 50px;
        width: 100%;
        text-shadow: 0px 0px 2px #640be6;
        font-size: 13px;
        text-align: center;
    }

    .gamePlay {
        border-radius: 15px;
        width: 350px;
        padding: 15px 24px 1px 20px;
        box-sizing: border-box;
        background: linear-gradient(180deg, #e4e4fb, #cadafb);
        position: relative;
        margin: 0 auto;
        transform: translateY(-40px);

        .title {
            display: flex;
            align-items: center;
            justify-content: center;

            .leftIcon,
            .rightIcon {
                width: 28px;
                height: 10px;
                // background: url("../assets/img/picture_title.png") no-repeat;
                background-size: 100% 100%;
            }

            .leftIcon {
                transform: rotateY(180deg);
            }

            .text {
                margin: 0 24px;
                font-family: "BalooBhaina";
                font-size: 16px;
                color: rgba(98, 44, 241, 1);
            }
        }

        .ruleContent {
            margin-top: 20px;

            .tag {
                display: flex;
                align-items: center;
                justify-content: flex-start;
                margin-bottom: 10px;

                .num {
                    width: 17px;
                    height: 17px;
                    background-color: rgba(200, 191, 248, 0.5);
                    border-radius: 50%;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    margin-right: 9px;
                    color: #432398;

                    font-size: 14px;
                }

                .tText {
                    font-size: 14px;

                    color: #432398;
                }
            }

            .rText {
                color: rgba(67, 35, 152, 0.7);
                font-size: 13px;
                // opacity: 0.7;
                margin-bottom: 15px;
                line-height: 1.3;
            }
        }
    }

    .luckyCarnival {
        width: 350px;
        padding: 14px 12px 20px;
        background: linear-gradient(180deg, #e4e4fb, #cadafb);
        border-radius: 15px;
        box-sizing: border-box;
        margin: 0 auto;
        margin-top: -15px;
        margin-bottom: 20px;

        .title {
            display: flex;
            align-items: center;
            justify-content: center;

            .leftIcon,
            .rightIcon {
                width: 28px;
                height: 10px;
                // background: url("../assets/img/picture_title.png") no-repeat;
                background-size: 100% 100%;
            }

            .leftIcon {
                transform: rotateY(180deg);
            }

            .text {
                margin: 0 24px;
                font-family: "BalooBhaina";
                font-size: 16px;
                color: rgba(98, 44, 241, 1);
            }
        }

        .giftContent {
            display: flex;
            align-items: center;
            justify-content: space-around;
            margin-top: 20px;

            .gItem {
                width: 50px;
                height: 50px;
                position: relative;
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;

                .giftImg {
                    img {
                        width: 47px;
                        height: auto;
                    }
                }

                .giftText {
                    margin-top: 12px;
                    color: rgba(67, 35, 152, 0.7);
                    font-size: 13px;
                }

                .giftStatus {
                    .canClaim {
                        width: 39px;
                        height: 15px;
                        background: linear-gradient(0deg, #f60000, #ff6e2e);
                        border: 1px solid #fff283;
                        box-sizing: border-box;
                        position: absolute;
                        border-radius: 9999px;

                        display: flex;
                        align-items: center;
                        justify-content: center;

                        color: #fffb86;
                        font-size: 10px;
                        left: 50%;
                        top: 40%;
                        transform: translateX(-52%) translateY(0%);
                    }

                    .success {
                        width: 20px;
                        height: 20px;
                        // background: url("../assets/img/reward/button_finished.png") no-repeat;
                        background-size: 100% 100%;
                        position: absolute;
                        left: 50%;
                        top: 33%;
                        transform: translateX(-50%) translateY(0%);
                    }
                }
            }
        }
    }

    .switchBtn {
        display: flex;
        align-items: center;
        justify-content: space-between;
        box-sizing: border-box;
        margin-bottom: 15px;
        width: 100%;
        z-index: 5;
        padding: 0px 27px;
        position: relative;

        div,
        span {
            white-space: nowrap !important;
        }

        .btn {
            width: 150px;
            height: 35px;
            box-sizing: border-box;
            background: url("../assets/images/button_no_select.png") no-repeat;
            background-size: 100% 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 13px;
            text-align: center;
            color: rgba(255, 255, 255, 0.6);
            font-weight: 400;
            padding-top: 4px;
            font-family: "BalooBhaina";
        }

        .activeBtn {
            // background: url("../assets/img/button_select.png") no-repeat;
            background-size: 100% 100%;
            font-family: "BalooBhaina";
            color: #af6608;
        }
    }

    .footer {
        margin-top: 20px;
        text-align: center;
        padding: 0 21px;
        font-size: 11px;
        overflow: hidden;
        line-height: 1.4;
        color: #fff;

        .color_yellow {
            color: #fff82b;
        }

        .line {
            width: 80%;
            margin: 10px auto;
            height: 1px;
            background: #fff;
            opacity: 0.35;
        }

        .footer_text {
            text-align: center;
            font-size: 11px;
            margin-bottom: 20px;
            color: #fff;
            opacity: 0.8;
        }
    }
}
</style>
  