<template>
    <div class="howtoplay">
        <div class="mask">
            <div class="content">
                <div class="title">
                    <div class="tx" v-if="language == 1">
                        <div class="icon"></div>
                        <div class="text">Rules</div>
                        <div class="icon"></div>
                    </div>
                    <div class="tx" v-if="language == 2">
                        <div class="icon"></div>
                        <div class="text">قواعد</div>
                        <div class="icon"></div>
                    </div>
                    <div class="tx" style="font-weight: bold" v-if="language == 3">
                        <div class="icon"></div>
                        <div class="text">नियम</div>
                        <div class="icon"></div>
                    </div>
                    <div class="tx" style="font-weight: bold; font-size: 0.4rem" v-if="language == 4">
                        <div class="icon"></div>
                        <div class="text">নিয়ম</div>
                        <div class="icon"></div>
                    </div>
                    <div class="tx" v-if="language == 5">
                        <div class="icon"></div>
                        <div class="text">Mga tuntunin</div>
                        <div class="icon"></div>
                    </div>
                </div>
                <div class="rule_text" v-if="language == 1">
                    <div class="rTag">Gameplay 1: Lucky Carnival:</div>
                    <div class="text">
                        1. Six chests have been set up. Sending lucky gifts to earn an x-times reward unlocks the
                        corresponding-tier chest. <br />
                        2. Each chest can only be unlocked once.
                    </div>
                    <div class="rTag">Gameplay 2: Lucky Partners:</div>
                    <div class="text">
                        1. Based on the number of specified gifts sent by users to the talent during the event. <br />
                        2. Each gift has its own separate leaderboard calculation. <br />
                        3. Top 3 gifters and receivers of each leaderboard will be rewarded. <br />
                    </div>
                    <div class="rTag">Gameplay 3: Lucky Star:</div>
                    <div class="text">
                        1. Gifter leaderboard, based on the total beans won in lucky gifts during the Event. Top3 can get
                        the rewards. <br>
                        2. Talent leaderboard, based on the total value of the lucky gifts received during the activity
                        period. Top3 can get rewards.
                    </div>

                    <div class="rTag">Note:</div>
                    <div class="text">Event rewards will be sent within 72 hours after the event ends. </div>
                </div>

                <div class="rule_text" v-if="language == 2">
                    <div class="rTag">Gameplay 1: Lucky Carnival:</div>
                    <div class="text">
                        1. 6 chests ko tayar kiya gaya hai. X-times inaam kamane ke liye lucky gifts bhejna uss se
                        milte-julte tier ki chest ko unlock karta hai. <br />
                        2. Har chest bas aik bar unlock ho sakti hai.
                    </div>
                    <div class="rTag">Gameplay 2: Lucky Partners:</div>
                    <div class="text">
                        1. Event ke doran users ke talents ko bheje gaye makhsoos gifts ki tadad pe mabni hai. <br />
                        2. Har gift ka apna alag leaderboard calculation hai. <br />
                        3. Har leaderboard ke top 3 gifters aur receivers ko rewards diye jaye ge. <br />
                    </div>
                    <div class="rTag">Gameplay 3: Lucky Star:</div>
                    <div class="text">
                        1. Gifter leaderboard, Event ke doran lucky gifts mein jeete gaye total beans ke hisab se banaya
                        gaya hai. Top 3 rewards hasil kar sakte hain. <br>
                        2. Talent leaderboard, activity period ke dauran hasil kiye gaye lucky gifts ki total value ke hisab
                        se banaya gaya hai. Top 3 rewards hasil kar sakte hain.
                    </div>

                    <div class="rTag">Note:</div>
                    <div class="text">Event rewards event khatam hone ke 72 hours ke doran bhej diye jaen ge. </div>
                </div>

                <div class="rule_text" v-if="language == 3">
                    <div class="rTag">गेमप्ले 1: लकी कार्निवल:</div>
                    <div class="text">
                        1. छह चेस्ट स्थापित किए गए हैं। एक्स-गुना इनाम अर्जित करने के लिए भाग्यशाली उपहार भेजने से
                        संबंधित-स्तरीय चेस्ट अनलॉक हो जाता है। <br />
                        2. प्रत्येक संदूक को केवल एक बार ही खोला जा सकता है।
                    </div>
                    <div class="rTag">गेमप्ले 2: लकी पार्टनर्स:</div>
                    <div class="text">
                        1. इवेंट के दौरान यूजर द्वारा प्रतिभाओं को भेजे गए निर्दिष्ट उपहारों की संख्या के आधार पर। <br />
                        2. प्रत्येक उपहार की अपनी अलग लीडरबोर्ड गणना होती है। <br />
                        3. प्रत्येक लीडरबोर्ड के शीर्ष 3 यूजर और प्राप्तकर्ताओं को पुरस्कृत किया जाएगा। <br />
                    </div>
                    <div class="rTag">गेमप्ले 3: लकी स्टार:</div>
                    <div class="text">
                        1. गिफ्टर लीडरबोर्ड, इवेंट के दौरान भाग्यशाली उपहारों में जीते गए कुल बीन्स के आधार पर। Top3 को
                        पुरस्कार मिल सकता है. <br>
                        2. गतिविधि अवधि के दौरान प्राप्त भाग्यशाली उपहारों के कुल मूल्य के आधार पर प्रतिभा लीडरबोर्ड। Top3
                        को पुरस्कार मिल सकता है.
                    </div>

                    <div class="rTag">टिप्पणी:</div>
                    <div class="text">ईवेंट पुरस्कार ईवेंट समाप्त होने के 72 घंटों के भीतर भेज दिए जाएंगे। </div>
                </div>

                <div class="rule_text" v-if="language == 4">
                    <div class="rTag">গেমপ্লে 1: লাকি কার্নিভাল:</div>
                    <div class="text">
                        1. ছয়টি বুক স্থাপন করা হয়েছে। x-গুন পুরষ্কার অর্জনের জন্য ভাগ্যবান উপহার পাঠানো সংশ্লিষ্ট-স্তরের
                        বুককে আনলক করে। <br />
                        2. প্রতিটি বুক শুধুমাত্র একবার আনলক করা যাবে।
                    </div>
                    <div class="rTag">গেমপ্লে 2: ভাগ্যবান অংশীদার:</div>
                    <div class="text">
                        1. ইভেন্ট চলাকালীন ব্যবহারকারীদের দ্বারা প্রতিভাদের পাঠানো নির্দিষ্ট উপহারের সংখ্যার উপর ভিত্তি করে।
                        <br />
                        2. প্রতিটি উপহারের নিজস্ব আলাদা লিডারবোর্ড গণনা আছে।<br />
                        3. প্রতিটি লিডারবোর্ডের সেরা 3 গিফটার এবং রিসিভারকে পুরস্কৃত করা হবে।<br />
                    </div>
                    <div class="rTag">গেমপ্লে 3: লাকি স্টার:</div>
                    <div class="text">
                        1. গিফটার লিডারবোর্ড, ইভেন্টের সময় ভাগ্যবান উপহারে জিতে নেওয়া মোট বিনের উপর ভিত্তি করে। Top3
                        পুরস্কার পেতে পারেন. <br>
                        2. প্রতিভা লিডারবোর্ড, কার্যকলাপের সময়কালে প্রাপ্ত ভাগ্যবান উপহারের মোট মূল্যের উপর ভিত্তি করে।
                        Top3 পুরস্কার পেতে পারেন.
                    </div>

                    <div class="rTag">বিঃদ্রঃ:</div>
                    <div class="text">ইভেন্ট পুরষ্কার ইভেন্ট শেষ হওয়ার 72 ঘন্টার মধ্যে পাঠানো হবে। </div>
                </div>

                <div class="rule_text" v-if="language == 5">
                    <div class="rTag">Gameplay 1: Lucky Carnival:</div>
                    <div class="text">
                        1. Nai-set up na ang mga anim na chest. Ang pagpapadala ng ng mga maswerteng regalo para makakuha ng
                        x-time na reward ay magbubukas sa kaukulang tier chest. <br />
                        2. Ang bawat chest ay maaari lamang i-unlock ng isang beses.
                    </div>
                    <div class="rTag">Gameplay 2: Lucky Partners: </div>
                    <div class="text">
                        1. Batay sa bilang ng mga tinutukoy na regalgo na ipinadala ng mga users sa talento sa panahon ng
                        kaganapan. <br />
                        2. Ang bawat regalo ay may sariling hiwalay na pagkalkula ng leaderboard.<br />
                        3. Ang nangungunang 3 gifter at receiver ng bawat leaderboard ay gagantimpalaan.<br />
                    </div>
                    <div class="rTag">Gameplay 3: Lucky Star: </div>
                    <div class="text">
                        1. Gifter leaderboard, batay sa kabuuang beans na napanalunan sa mga masuwerteng regalo sa
                        Kaganapan. Makukuha ng Top3 ang mga reward. <br>
                        2. Talent leaderboard, batay sa kabuuang halaga ng mga masuwerteng regalo na natanggap sa panahon ng
                        aktibidad. Ang Top3 ay maaaring makakuha ng mga reward.
                    </div>

                    <div class="rTag">Tandaan:</div>
                    <div class="text">Ipapadala ang mga reward sa event sa loob ng 72 oras pagkatapos ng event. </div>
                </div>
                <div class="closeBtn" @click="closeMask">
                    <img src="../assets/images/Close btn.png" alt="" />
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { ref, onMounted } from "vue";
export default {
    name:'howToPlay',
    props: ["language"],
    setup(props, { emit }) {
        let _scrollTop = ref(0);
        function closeMask() {
            document.body.style.position = "";
            document.body.style.top = "";
            document.scrollingElement.scrollTop = _scrollTop.value;
            emit("closeMe");
        }
        onMounted(() => {
            _scrollTop.value = document.scrollingElement.scrollTop;
            document.body.style.position = "fixed";
            document.body.style.top = -_scrollTop.value + "px";
        });
        function nouse() { }
        return { closeMask, nouse };
    },
};
</script>
  
<style lang="less" scoped>
.howtoplay {
    .dian_text {
        text-align: left;
        font-family: "Roboto-Regular";

        font-weight: 400;
        color: rgba(255, 255, 255, 0.6);
        line-height: 1.5;
        font-size: 11px;
        margin-top: 3px;
        position: relative;
    }

    .mask {
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background-color: rgba(0, 0, 0, 0.5);
        z-index: 9999;

        .text {
            font-size: 13px;
        }

        .content {
            font-family: "Roboto" !important;
            left: 50%;
            top: 50%;
            transform: translateX(-50%) translateY(-50%);
            position: relative;
            box-sizing: border-box;
            padding: 18px 15px 25px 8px;
            padding-right: 0;
            width: 300px;
            height: 400px;
            background: linear-gradient(90deg, #8268E8, #977AF3, #8268E8);
            border: 1.5px solid #FFE898;
            border-radius: 15px;

            .title {
                width: 140px;
                height: 35px;
                position: absolute;
                text-align: center;
                display: flex;
                align-items: center;
                justify-content: center;
                left: 50%;
                top: 0;
                transform: translateX(-50%) translateY(-55%);
                background: url("../assets/images/button_no_select.png") no-repeat;
                background-size: 100% 100%;

                .tx {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    font-family: "BalooBhaina";


                    .text {
                        font-size: 15px;
                        color: #fff;
                        margin: 0 50px;
                        white-space: nowrap;
                        font-weight: 600;
                    }
                }
            }

            .rule_text {
                text-align: left;
                overflow: auto;
                height: 100%;
                padding-right: 16px;

                .topText {
                    text-align: left;
                    font-weight: 300;
                    line-height: 20px;
                    font-size: 13px;
                    margin-top: 10px;
                    font-family: "Roboto-Regular";
                    color: #fff;

                    .num {
                        display: inline-flex;
                        align-items: center;
                        justify-content: center;
                        width: 15px;
                        height: 15px;
                        background-color: rgba(0, 0, 0, 0.1);
                        border-radius: 50%;
                        color: #fff;
                    }
                }

                .text {
                    text-align: left;
                    // font-weight: lighter;
                    line-height: 20px;
                    font-size: 13px;
                    margin-top: 10px;
                    font-family: "Roboto-Regular";
                    color: #fff;
                    background-color: rgba(0, 0, 0, 0.1);

                    padding: 10px;
                    border-radius: 5px;
                }

                .tag {
                    border-radius: 5px;
                    display: inline-block;
                    // color: rgba(255, 255, 255, 0.6);
                    font-size: 11px;
                    margin-top: 10px;
                    color: #fff;
                }
            }

            .rTag {
                font-size: 12px;
                font-weight: 500;
                margin-top: 10px;
                margin-bottom: -5px;
                color: #fff;
                font-family: "Roboto-Regular";
                padding-left: 10px;
            }

            img {
                display: inline-block;
                margin: 20px 0 16px;
            }

            .noteText {
                .tag {
                    margin-top: 0;
                    font-family: "Roboto-Regular";
                }

                font-size: 11px !important;
                color: rgba(255, 255, 255, 0.6);
                padding: 10px;
                border-radius: 5px;
                padding-left: 0;
            }
        }

        .closeBtn {
            width: 28px;
            height: 28px;
            position: absolute;
            left: 50%;
            bottom: -25px;
            transform: translateX(-50%) translateY(0%);

            img {
                width: 100%;
                height: 100%;
            }
        }
    }
}</style>
  