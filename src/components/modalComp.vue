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
                    <div class="paragraph_6">
                        Hello, Pattern Game fans! The Round 2 of the OyeTalk’s most entertaining event is here.
                        In this “Super Pattern-Round 2” event, you can participate just by playing the Pattern game
                        and completing the Special tasks so you can win exclusive rewards.
                        <br />
                        This event consists of 4 main parts:
                        <br />
                        1. Room Special Target
                        <br />
                        2. Daily Task
                        <br />
                        3. Winning Daily Leaderboard
                        <br />
                        4. Room Consumption Leaderboard
                    </div>
                    <div>
                        <span class="text_1">· Room Special Target</span>
                        <div class="text-wrapper_1 flex-col">
                            <span class="paragraph_1">During the event, if the total amount of bets placed on Pattern
                                games in
                                the live room reaches 150 Million beans, the live room owner will receive a special
                                target bonus
                                of 100k beans!<br /></span>
                        </div>

                    </div>
                    <span class="text_2">· Daily Task</span>
                    <div class="text-wrapper_2 flex-col">
                        <span class="text_3">Now you can win exclusive rewards just by completing daily tasks. Users
                            just need to complete daily tasks and they will receive respective target rewards!
                            <br><br></span>
                        <span class="paragraph_2">Note: There will be a delay of 30 mins in sending the rewards. Rewards
                            will expire at UTC 0:00 the next day.<br /></span>
                    </div>
                    <span class="text_4">· Winning Daily Leaderboard</span>
                    <div class="text-wrapper_3 flex-col">
                        <span class="paragraph_3">
                            1. A Winning daily leaderboard of top 3 users will receive exciting rewards! These rewards
                            will be sent to the user automatically at the end of the day during the event.<br />
                            2. Winning Leaderboard is ranked based on the beans users have won in the Royal Pattern that
                            day.
                        </span>
                    </div>
                    <span class="text_5">· Room Consumption Leaderboard</span>
                    <div class="text-wrapper_4 flex-col">
                        <span class="paragraph_4">
                            1. There will be a Room Consumption Leaderboard. Which will show how many beans are consumed
                            in the live room during the event.<br />
                            2. During the event period, the top 5 live room owners with the highest accumulated bets on
                            Pattern games will be rewarded. Rewards will be sent automatically.
                        </span>
                    </div>
                    <span class="paragraph_5">
                        Note:<br />
                        · When the Pattern event starts, the VIP mode will be turned on until the event ends.<br />
                        · Event rewards will be received within 72 hours after the event ends. According to UTC, rewards
                        will be sent before 3/12/22 at 12:00:00. Event time is based on UTC time.
                    </span>
                </div>

                <div class="rule_text" v-if="language == 2">
                    <div class="paragraph_6">
                        ہیلو، پیٹرن گیم کے شائقین! OyeTalk کا سب سے دلچسپ واقعہ Round 2 یہاں ہے۔
                        اس "سپر پیٹرن-راؤنڈ 2" واقعہ میں، آپ پیٹرن گیم کھیل کر اور خصوصی کام مکمل کرکے انحصاری انعامات
                        جیت سکتے ہیں۔
                        <br />
                        یہ واقعہ 4 اہم حصوں سے مشتمل ہے:
                        <br />
                        1. روم خصوصی ہدف
                        <br />
                        2. روزانہ کا کام
                        <br />
                        3. جیتنے والے روزانہ لیڈر بورڈ
                        <br />
                        4. روم استہلاک لیڈر بورڈ
                    </div>
                    <div>
                        <span class="text_1">· روم خصوصی ہدف</span>
                        <div class="text-wrapper_1 flex-col">
                            <span class="paragraph_1">
                                واقعہ کے دوران، اگر پیٹرن کے کھیلوں میں لائیو روم میں لگائے گئے کل شراکت کی مقدار 150
                                ملین بینز تک
                                پہنچ جائے، تو لائیو روم کے مالک کو 100 کلو بینز کا خصوصی ہدف بونس ملے گا!
                                <br />
                            </span>
                        </div>

                    </div>
                    <span class="text_2">· روزانہ کا کام</span>
                    <div class="text-wrapper_2 flex-col">
                        <span class="text_3">اب آپ صرف روزانہ کے کام مکمل کرکے انحصاری انعامات جیت سکتے ہیں۔ صارفین کو
                            صرف روزانہ کے کام
                            مکمل کرنا ہوگا اور وہ انحصاری ہدف انعامات حاصل کریں گے!
                            <br><br>
                        </span>
                        <span class="paragraph_2">نوٹ: انعامات بھیجنے میں 30 منٹ کا تاخیر ہوگا۔ انعامات کو اگلے دن UTC
                            0:00 پر ختم ہوجائے گا۔
                            <br />
                        </span>
                    </div>
                    <span class="text_4">· جیتنے والے روزانہ لیڈر بورڈ</span>
                    <div class="text-wrapper_3 flex-col">
                        <span class="paragraph_3">
                            1. اوپری روزانہ لیڈر بورڈ کے تین صارفین کو دلچسپ انعامات ملیں گے! یہ انعامات واقعہ کے دن کے
                            آخر میں صارف کو خود بخود
                            بھیجے جائیں گے۔
                            <br />
                            2. جیتنے والے لیڈر بورڈ پر صارفین کو انعام دیا جاتا ہے جو وہ دن بھر میں رائل پیٹرن میں جیتے
                            ہیں۔
                        </span>
                    </div>
                    <span class="text_5">· روم استہلاک لیڈر بورڈ</span>
                    <div class="text-wrapper_4 flex-col">
                        <span class="paragraph_4">
                            1. ایک روم استہلاک لیڈر بورڈ ہوگا۔ جو دکھائے گا کہ واقعے کے دوران لائیو روم میں کتنے بینز
                            استعمال ہوئے ہیں۔<br />
                            2. واقعے کے دوران، اسٹائل پر بازیوں پر سب سے زیادہ جمع کیے گئے شراکت داروں کے بینزوں کی سب
                            سے زیادہ بیٹ کرنے والے توپ 5 لائیو روم مالکوں کو انعام دیا جائے گا۔ انعامات خود بخود بھیجے
                            جائیں گے۔
                        </span>
                    </div>
                    <span class="paragraph_5">
                        نوٹ:<br />
                        · جب پیٹرن واقعہ شروع ہوتا ہے، وی آئی پی موڈ کو شروع کر دیا جاتا ہے جب تک واقعہ ختم نہیں
                        ہوتا۔<br />
                        · واقعہ انعامات واقعہ ختم ہونے کے 72 گھنٹے بعد موصول ہوں گے۔ یو ٹی سی کے مطابق، انعامات 3/12/22
                        سے پہلے بھیجے جائیں گے۔ واقعہ کا وقت یو ٹی سی وقت پر مبنی ہوتا ہے۔
                    </span>
                </div>
                <div class="rule_text" v-if="language == 3">
                    <div class="paragraph_6">
                        हैलो, पैटर्न गेम प्रेमियों! ओये टॉक की सबसे मनोरंजक घटना का दूसरा दौर यहां है। इस "सुपर
                        पैटर्न-दौर 2" आयोजन में, आप
                        पैटर्न गेम खेलकर और विशेष कार्यों को पूरा करके अनन्य इनाम जीत सकते हैं। <br />
                        यह घटना 4 मुख्य भागों से मिलकर बनती है:
                        <br />
                        1. रूम विशेष लक्ष्य
                        <br />
                        2. दैनिक कार्य
                        <br />
                        3. जीतने वाला दैनिक लीडरबोर्ड
                        <br />
                        4. रूम कंजम्प्शन लीडरबोर्ड
                    </div>
                    <div>
                        <span class="text_1">· रूम विशेष लक्ष्य</span>
                        <div class="text-wrapper_1 flex-col">
                            <span class="paragraph_1">इस घटना के दौरान, यदि लाइव रूम में पैटर्न गेमों पर लगाए गए कुल
                                दांव 150 मिलियन
                                बीन्स
                                तक पहुंच जाते हैं, तो लाइव रूम के मालिक को 100k बीन्स का विशेष लक्ष्य बोनस मिलेगा!
                                <br /></span>
                        </div>

                    </div>
                    <span class="text_2">· दैनिक कार्य</span>
                    <div class="text-wrapper_2 flex-col">
                        <span class="text_3">अब आप दैनिक कार्यों को पूरा करके केवल अनन्य इनाम जीत सकते हैं। उपयोगकर्ताओं
                            को केवल दैनिक
                            कार्यों
                            को पूरा करने की आवश्यकता है और वे आवश्यक लक्ष्य इनाम प्राप्त करेंगे! <br><br></span>
                        <span class="paragraph_2">नोट: इनाम भेजने में 30 मिनट का अंतर होगा। इनाम अगले दिन UTC 0:00 पर
                            समाप्त हो जाएगा। <br /></span>
                    </div>
                    <span class="text_4">· जीतने वाला दैनिक लीडरबोर्ड</span>
                    <div class="text-wrapper_3 flex-col">
                        <span class="paragraph_3">
                            1. शीर्ष 3 उपयोगकर्ताओं के एक विजयी दैनिक लीडरबोर्ड को उत्साहजनक पुरस्कार मिलेगा! इन
                            पुरस्कारों को इवेंट के
                            दौरान
                            दिन के अंत में उपयोगकर्ता को स्वचालित रूप से भेज दिया जाएगा। <br />
                            2. जीतने वाले लीडरबोर्ड को रॉयल पैटर्न में उपयोगकर्ताओं द्वारा जीते गए बीन्स के आधार पर
                            क्रमित किया
                            जाता है।
                        </span>
                    </div>
                    <span class="text_5">· रूम कंजम्प्शन लीडरबोर्ड</span>
                    <div class="text-wrapper_4 flex-col">
                        <span class="paragraph_4">
                            1. रूम कंजम्प्शन लीडरबोर्ड होगा। जो इवेंट के दौरान लाइव रूम में कितने बीन्स खपाए गए हैं, वह
                            दिखाएगा। <br />
                            2. इवेंट अवधि के दौरान, पैटर्न गेमों पर सबसे अधिक एकत्रित दांव लगाने वाले पांच लाइव रूम के
                            मालिकों को
                            पुरस्कृत
                            किया जाएगा। पुरस्कार स्वचालित रूप से भेजे जाएंगे।
                        </span>
                    </div>
                    <span class="paragraph_5">
                        ध्यान दें:<br />
                        · जब पैटर्न इवेंट शुरू होता है, तो वीआईपी मोड को इवेंट समाप्त होने तक चालू किया जाएगा। <br />
                        · इवेंट पुरस्कार इवेंट समाप्त होने के 72 घंटे के भीतर प्राप्त किए जाएंगे। UTC के अनुसार,
                        पुरस्कार 3/12/22
                        को
                        12:00:00 से पहले भेजे जाएंगे। इवेंट का समय UTC समय के आधार पर है।
                    </span>
                </div>

                <div class="rule_text" v-if="language == 4">
                    <div class="paragraph_6">
                        হ্যালো, প্যাটার্ন গেম প্রেমিকগণ! অয়ে টকের সবচেয়ে মজার ইভেন্টের দ্বিতীয় রাউন্ড এখানে। এই
                        "সুপার প্যাটার্ন-রাউন্ড 2" ইভেন্টে,
                        আপনি শুধুমাত্র প্যাটার্ন গেম খেলে এবং বিশেষ কাজগুলি সম্পাদন করে আপনি অনন্য পুরস্কার জিততে পারেন।
                        <br />
                        এই ইভেন্টের প্রধান 4 অংশ রয়েছে:
                        <br />
                        1. রুম বিশেষ লক্ষ্য
                        <br />
                        2. দৈনিক কাজ
                        <br />
                        3. জিতার দৈনিক লীডারবোর্ড
                        <br />
                        4. রুম ব্যবহার লীডারবোর্ড
                    </div>
                    <div>
                        <span class="text_1">· রুম বিশেষ লক্ষ্য</span>
                        <div class="text-wrapper_1 flex-col">
                            <span class="paragraph_1">ইভেন্টে, যদি লাইভ রুমে প্যাটার্ন গেমে বিস্তৃত দাঁড়িয়ে যাওয়া
                                সর্বমোট মুদ্রার পরিমাণ
                                ১৫০ মিলিয়ন বীন পর্যন্ত পৌঁছে, তবে লাইভ রুম মালিকগণ একটি বিশেষ লক্ষ্য বোনাস ১০০ হাজার
                                বীন প্রাপ্ত করবেন!
                                <br /></span>
                        </div>

                    </div>
                    <span class="text_2">· দৈনিক কাজ</span>
                    <div class="text-wrapper_2 flex-col">
                        <span class="text_3">এখন আপনি দৈনিক কাজগুলি সম্পাদন করে অনন্য পুরস্কার জিততে পারেন।
                            ব্যবহারকারীদের কেবলমাত্র দৈনিক কাজগুলি
                            সম্পাদন করতে হবে এবং তারা প্রাপ্তিশীল লক্ষ্য পুরস্কার প্রাপ্ত করবেন!
                            <br><br></span>
                        <span class="paragraph_2">নোট: পুরস্কার প্রেরণে একটি দেরি থাকতে পারে। পুরস্কার পরবর্তী দিন এউটি
                            দিনের শেষে UTC 0:00 তে মেয়াদ উত্তীর্ণ
                            হবে। <br /></span>
                    </div>
                    <span class="text_4">· জিতার দৈনিক লীডারবোর্ড</span>
                    <div class="text-wrapper_3 flex-col">
                        <span class="paragraph_3">
                            ১। শীর্ষ ৩ ব্যবহারকারীর একটি বিজয়ী দৈনিক লীডারবোর্ড উৎসাহজনক পুরস্কার প্রাপ্ত করবে! এই
                            পুরস্কারগুলি ইভেন্টের দিনের
                            শেষে ব্যবহারকারীর নিজস্বভাবে প্রেরিত হবে। <br />
                            ২। জিতার লীডারবোর্ডটি তারিখে ব্যবহারকারীদের রাজস্বের উপর ভিত্তি করে শ্রেণীবদ্ধ করা হয়।
                        </span>
                    </div>
                    <span class="text_5">· রুম ব্যবহার লীডারবোর্ড</span>
                    <div class="text-wrapper_4 flex-col">
                        <span class="paragraph_4">
                            ১। একটি রুম ব্যবহার লীডারবোর্ড থাকবে। যা ইভেন্ট সময়ে লাইভ রুমে কতগুলি বীন ব্যয় করা হয়েছে
                            তা প্রদর্শন করবে। <br />
                            ২। ইভেন্ট সময়ে, প্যাটার্ন গেমে সর্বোচ্চ একুমুকির সংগ্রহিত বেট সহ শীর্ষ ৫ লাইভ রুম মালিকগণকে
                            পুরস্কৃত করা হবে। পুরস্কার
                            স্বয়ংক্রিয়ভাবে প্রেরিত হবে।
                        </span>
                    </div>
                    <span class="paragraph_5">
                        নোট:<br />
                        · প্যাটার্ন ইভেন্ট শুরু হলে, ইভেন্ট শেষ হওয়া পর্যন্ত ভিআইপি মোড চালু থাকবে।<br />
                        · ইভেন্ট পুরস্কার ইভেন্ট শেষের পরে ৭২ ঘণ্টার মধ্যে প্রাপ্ত করা হবে। UTC অনুযায়ী, পুরস্কার
                        3/12/22 এর আগে 12:00:00 এ
                        প্রেরিত হবে। ইভেন্টের সময় ভিত্তিতে UTC সময়।
                    </span>
                </div>

                <div class="rule_text" v-if="language == 5">
                    <div class="paragraph_6">
                        Kumusta mga tagahanga ng Pattern Game! Narito na ang Round 2 ng pinakamakulay na event ng
                        OyeTalk.
                        Sa "Super Pattern-Round 2" na ito, maaari kang sumali sa pamamagitan lamang ng paglalaro ng
                        Pattern game at pagkumpleto ng mga Espesyal na gawain upang manalo ng mga eksklusibong premyo.
                        <br />
                        Ang event na ito ay binubuo ng 4 pangunahing bahagi:
                        <br />
                        1. Layunin ng Espesyal na Silid
                        <br />
                        2. Araw-araw na Gawain
                        <br />
                        3. Panalo sa Araw-araw na Leaderboard
                        <br />
                        4. Room Consumption Leaderboard
                    </div>
                    <div>
                        <span class="text_1">· Layunin ng Espesyal na Silid</span>
                        <div class="text-wrapper_1 flex-col">
                            <span class="paragraph_1">Sa panahon ng event, kung ang kabuuang halaga ng mga pusta sa mga
                                laro ng Pattern sa live room ay umabot sa 150 Milyong barya, ang may-ari ng live room ay
                                tatanggap ng espesyal na bonus na layunin na 100k barya!<br /></span>
                        </div>
                    </div>
                    <span class="text_2">· Araw-araw na Gawain</span>
                    <div class="text-wrapper_2 flex-col">
                        <span class="text_3">Ngayon maaari kang manalo ng mga eksklusibong premyo sa pamamagitan lamang
                            ng pagkumpleto ng mga araw-araw na gawain. Kailangan lamang ng mga user na kumpletuhin ang
                            mga araw-araw na gawain at tatanggapin nila ang mga katumbas na layunin na premyo!
                            <br><br></span>
                        <span class="paragraph_2">Tandaan: Magkakaroon ng 30 minuto na kahulugan sa pagpapadala ng mga
                            premyo. Ang mga premyo ay mag-eexpire sa UTC 0:00 kinabukasan.<br /></span>
                    </div>
                    <span class="text_4">· Panalo sa Araw-araw na Leaderboard</span>
                    <div class="text-wrapper_3 flex-col">
                        <span class="paragraph_3">
                            1. Ang mga pangunahing 3 na user sa Panalo sa Araw-araw na leaderboard ay tatanggap ng
                            nakaaaliw na premyo! Ang mga premyong ito ay ipapadala sa user nang awtomatiko sa katapusan
                            ng araw sa panahon ng event.<br />
                            2. Ang Panalo sa Leaderboard ay ranggo batay sa mga barya na napanalunan ng mga user sa
                            Royal Pattern sa araw na iyon.
                        </span>
                    </div>
                    <span class="text_5">· Room Consumption Leaderboard</span>
                    <div class="text-wrapper_4 flex-col">
                        <span class="paragraph_4">
                            1. May magiging Room Consumption Leaderboard. Ito ay magpapakita kung gaano karaming barya
                            ang naubos sa live room sa panahon ng event.<br />
                            2. Sa panahon ng event, ang mga nangungunang 5 na may-ari ng live room na may pinakamataas
                            na nakakolektang mga pusta sa mga laro ng Pattern ay gagantimpalaan. Ang mga premyo ay
                            ipapadala nang awtomatiko.
                        </span>
                    </div>
                    <span class="paragraph_5">
                        Tandaan:<br />
                        · Kapag nagsimula ang Pattern event, ang VIP mode ay magiging aktibo hanggang sa matapos ang
                        event.<br />
                        · Ang mga premyo ng event ay matatanggap sa loob ng 72 oras matapos ang pagtatapos ng event.
                        Ayon sa UTC, ang mga premyo ay ipapadala bago ang 3/12/22 sa 12:00:00. Ang oras ng event ay
                        batay sa UTC.
                    </span>

                </div>
                <div class="closeBtn" @click="closeMask">
                    <img src="../assets/images/close.png" alt="" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { ref, onMounted } from "vue";
export default {
    name: 'howToPlay',
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
.paragraph_6 {
    width: 93%;
    // height: 416px;
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 16px;
    font-family: Roboto-Regular;
    font-weight: normal;
    text-align: left;
    //   line-height: 15px;
    margin: 0 auto;

}

.text_1 {
    width: 256px;
    height: 26px;
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 16px;
    font-family: Roboto-Medium;
    font-weight: 500;
    text-align: left;
    white-space: nowrap;
    line-height: 39px;
    //   margin: 31px 0 0 39px;
}

.text-wrapper_1 {
    background-color: rgba(255, 235, 205, 1);
    border-radius: 10px;
    padding: 2vw;

    .paragraph_1 {
        overflow-wrap: break-word;
        color: rgba(153, 65, 12, 1);
        font-size: 16px;
        font-family: Roboto-Regular;
        font-weight: normal;
        text-align: left;
    }
}

.text_2 {
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 16px;
    font-family: Roboto-Medium;
    font-weight: 500;
    text-align: left;
    white-space: nowrap;
    line-height: 38px;
}

.text-wrapper_2 {
    background-color: rgba(255, 235, 205, 1);
    border-radius: 10px;
    padding: 2vw;

    .text_3 {
        overflow-wrap: break-word;
        color: rgba(153, 65, 12, 1);
        font-size: 16px;
        font-family: Roboto-Regular;
        font-weight: normal;
        text-align: left;
    }

    .paragraph_2 {
        overflow-wrap: break-word;
        color: rgba(153, 65, 12, 1);
        font-size: 14px;
        font-family: Roboto-Regular;
        font-weight: normal;
        text-align: left;
    }
}

.text_4 {
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 16px;
    font-family: Roboto-Medium;
    font-weight: 500;
    text-align: left;
    white-space: nowrap;
    line-height: 39px;
}

.text-wrapper_3 {
    background-color: rgba(255, 235, 205, 1);
    border-radius: 10px;
    padding: 2vw;

    .paragraph_3 {
        overflow-wrap: break-word;
        color: rgba(153, 65, 12, 1);
        font-size: 16px;
        font-family: Roboto-Regular;
        font-weight: normal;
        text-align: left;
    }
}

.text_5 {
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 16px;
    font-family: Roboto-Bold;
    font-weight: 700;
    text-align: left;
    white-space: nowrap;
    line-height: 39px;
}


.text-wrapper_4 {
    background-color: rgba(255, 235, 205, 1);
    border-radius: 10px;
    padding: 2vw;

    .paragraph_4 {
        overflow-wrap: break-word;
        color: rgba(153, 65, 12, 1);
        font-size: 16px;
        font-family: Roboto-Regular;
        font-weight: normal;
        text-align: left;
    }
}

.paragraph_5 {
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 14px;
    font-family: Roboto-Regular;
    font-weight: normal;
    text-align: left;
}





// .rTag {
//     font-size: 12px;
//     font-weight: 500;
//     margin-top: 10px;
//     margin-bottom: -5px;
//     color: red;
//     font-family: "Roboto-Regular";
//     padding-left: 10px;
// }


//previous text design
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
            background: white;
            border: 1.5px solid #FFE898;
            border-radius: 15px;

            .title {
                width: 181px;
                height: 35px;
                position: absolute;
                text-align: center;
                display: flex;
                align-items: center;
                justify-content: center;
                left: 50%;
                top: 7px;
                transform: translateX(-50%) translateY(-55%);
                background: url("../assets/images/picture_title.png") no-repeat;
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
                    color: red;
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
                color: red;
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
}
</style>