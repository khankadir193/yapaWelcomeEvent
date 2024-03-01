<template>
    <div>
        <!-- open the modal component button -->
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
            <!-- <div class="float_rules">
                <button @click="openRulesTab">Rules</button>
            </div> -->

            <div class="float_rules" @click="openRule">
                <!-- <span :class="selectLanguageIndex == 5 ? ' mgaText' : ''">
                    {{ btnTextList[selectLanguageIndex - 1] }}</span> -->
            </div>
            <!-- howtoplay -->
            <!-- <howToPlay :language="selectLanguageIndex" v-if="ruleShow" @closeMe="ruleShow = false">
            </howtoplay> -->
        </div>
    </div>
</template>

<script>
import { ref } from 'vue';
// import howToPlay from './howToPlay.vue';

export default {
    name: 'HeaderComponent',
    setup() {
        let language = ref(["English", "Urdu", "Hindi", "Bengali", "Filipino"]);
        let ruleShow = ref(false);
        let selectLanguageIndex = ref(1);
        let activeKey = ref("");

        function openRule() {
            ruleShow.value = true;
            baseFun("rule");
        }

        function baseFun(location) {
            let lang = language.value[selectLanguageIndex.value - 1];
            console.log('lang...??',lang);
            window.oyetalkActivityJsAnalysis.track("click_event", {
                location,
                module: window.location.href.split("?")[0],
                name: activeKey.value,
                language: lang,
            });
        }

        return {
            baseFun,
            openRule,
            language,
            selectLanguageIndex
        }
    },
    components:{
        // howToPlay,
    }
}
</script>

<style lang="less" scoped>
.header {
    background-image: url('../assets/images/header.jpg');
    width: 100%;
    height: 100vh;
    background-size: contain;
    background-repeat: no-repeat;
}

.float_rules {
    position: absolute;
    background: linear-gradient(0deg, #733dfd, #e477ff);

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
    top: 335px;

    button {
        color: #fff;
        font-size: 13px;
        border: none;
        outline: none;
        background: none;
    }

    background-size: 100% 100%;
}

.modal {
    display: none;
    /* Hide the modal by default */
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgb(0, 0, 0);
    background-color: rgba(0, 0, 0, 0.4);

    .modal-content {
        background-color: #fefefe;
        margin: 15% auto;
        padding: 20px;
        border: 1px solid #888;
        width: 80%;
    }

    .close {
        color: #aaaaaa;
        float: right;
        font-size: 28px;
        font-weight: bold;
    }

    .close:hover,
    .close:focus {
        color: #000;
        text-decoration: none;
        cursor: pointer;
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
    }

    .language {
        color: #000;
        font-size: 12px;
    }

    .rtbg {
        position: absolute;
        width: 21px;
        height: 20px;
        right: 0px;
        top: 0px;
        background: rgba(193, 104, 255, 1);
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
    }

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


    .check_show {
        height: 3.3rem;
        bottom: -3.34rem;
        z-index: 15;
    }
}
</style>