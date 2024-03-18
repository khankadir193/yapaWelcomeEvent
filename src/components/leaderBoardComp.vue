<template>
    <div class="welcome-title">
        <h2>Welcome Offer</h2>
    </div>
    <div class="leaderBoard">
        <span class="text_14">Welcome to YAPA! Start your first topup with more surprising rewards!</span>
        <div v-for="item in beansData" :key="item.id" class="leaderBoard-strip">
            <div class="beans-icon">
                <div class="beans-img">
                    <img src="../assets/images/beans-icon.png" alt="beans">
                </div>
                <div class="beans-text">
                    <span>{{ item.conditions[0].value }}</span>
                </div>
            </div>

            <!-- here i am displaying two reward icons -->
            <div v-if="item.awardsInstance.length === 2" class="img-container">
                <div class="first-icon">
                    <span>{{ item.awardsInstance[0].days }}</span>
                    <img :src="item.awardsInstance[0].award.image" alt="icon">
                </div>
                <div class="second-icon">
                    <span>{{ item.awardsInstance[1].days }} days</span>
                    <img :src="item.awardsInstance[1].award.image" alt="icon">
                </div>
            </div>

            <!-- here i am displaying three reward icons -->
            <div v-if="item.awardsInstance.length === 3" class="img-container">
                <div class="first-icon">
                    <span>{{ item.awardsInstance[0].days }}</span>
                    <img :src="item.awardsInstance[0].award.image" alt="icon">
                </div>
                <div class="second-icon">
                    <span>{{ item.awardsInstance[1].days }} days</span>
                    <img :src="item.awardsInstance[1].award.image" alt="icon">
                </div>
                <div class="third-icon">
                    <span>{{ item.awardsInstance[2].days }} days</span>
                    <img :src="item.awardsInstance[2].award.image" alt="icon">
                </div>
            </div>

            <!-- here i am displaying four reward icons -->
            <div v-if="item.awardsInstance.length === 4 && item.id === 3" class="img-container">
                <div class="first-icon">
                    <span>{{ item.awardsInstance[0].days }}</span>
                    <img :src="item.awardsInstance[0].award.image" alt="icon">
                </div>
                <div class="second-icon">
                    <span>{{ item.awardsInstance[1].days }} days</span>
                    <img :src="item.awardsInstance[1].award.image" alt="icon">
                </div>
                <div class="third-icon">
                    <span>{{ item.awardsInstance[2].days }} days</span>
                    <img :src="item.awardsInstance[2].award.image" alt="icon">
                </div>
                <div class="fourth-icon">
                    <span>{{ item.awardsInstance[3].days }} days</span>
                    <img :src="item.awardsInstance[3].award.image" alt="icon">
                </div>
            </div>

            <!-- here i am displaying four reward icons -->
            <div v-if="item.awardsInstance.length === 4 && item.id === 16" class="img-container">
                <div class="first-icon">
                    <span>{{ item.awardsInstance[0].days }}</span>
                    <img :src="item.awardsInstance[0].award.image" alt="icon">
                </div>
                <div class="second-icon">
                    <span>{{ item.awardsInstance[1].days }} days</span>
                    <img :src="item.awardsInstance[1].award.image" alt="icon">
                </div>
                <div class="third-icon">
                    <span>{{ item.awardsInstance[2].days }} days</span>
                    <img :src="item.awardsInstance[2].award.image" alt="icon">
                </div>
                <div class="fourth-icon">
                    <span>{{ item.awardsInstance[3].days }} days</span>
                    <img :src="item.awardsInstance[3].award.image" alt="icon">
                </div>
            </div>

            <!-- here i am displaying five reward icons -->
            <div v-if="item.awardsInstance.length === 5 && item.id === 17" class="img-container">
                <div class="first-icon">
                    <span>{{ item.awardsInstance[0].days }}</span>
                    <img :src="item.awardsInstance[0].award.image" alt="icon">
                </div>
                <div class="second-icon">
                    <span>{{ item.awardsInstance[1].days }} days</span>
                    <img :src="item.awardsInstance[1].award.image" alt="icon">
                </div>
                <div class="third-icon">
                    <span>{{ item.awardsInstance[2].days }} days</span>
                    <img :src="item.awardsInstance[2].award.image" alt="icon">
                </div>
                <div class="fourth-icon">
                    <span>{{ item.awardsInstance[3].days }} days</span>
                    <img :src="item.awardsInstance[3].award.image" alt="icon">
                </div>
                <div class="fifth-icon">
                    <span>{{ item.awardsInstance[4].days }} days</span>
                    <img :src="item.awardsInstance[4].award.image" alt="icon">
                </div>
            </div>

            <!-- here i am displaying five reward icons -->
            <div v-if="item.awardsInstance.length === 5 && item.id === 18" class="img-container">
                <div class="first-icon">
                    <span>{{ item.awardsInstance[0].days }}</span>
                    <img :src="item.awardsInstance[0].award.image" alt="icon">
                </div>
                <div class="second-icon">
                    <span>{{ item.awardsInstance[1].days }} days</span>
                    <img :src="item.awardsInstance[1].award.image" alt="icon">
                </div>
                <div class="third-icon">
                    <span>{{ item.awardsInstance[2].days }} days</span>
                    <img :src="item.awardsInstance[2].award.image" alt="icon">
                </div>
                <div class="fourth-icon">
                    <span>{{ item.awardsInstance[3].days }} days</span>
                    <img :src="item.awardsInstance[3].award.image" alt="icon">
                </div>
                <div class="fifth-icon">
                    <span>{{ item.awardsInstance[4].days }} days</span>
                    <img :src="item.awardsInstance[4].award.image" alt="icon">
                </div>
            </div>

        </div>
        <h2 class="paragraph_1">
            This offer is valid for all payment methods. This offer is valid till 30th August. All rewards will be sent
            automatically to user's baggage.<br>
            All rights belong to Yapa.
        </h2>
    </div>

    <div class="top-up">
        <img src="../assets/images/button_top_up.png" alt="top-up">
    </div>

    <div class="footer">
        <span class="text_2">
            Roman & English:<span class="num">+1(442)228-3245</span> Thank you!
        </span>
        <span class="line">------------------------------------</span>
        <span class="rights">All rights reserved by YAPA</span>
    </div>
</template>

<script>
import axios from 'axios';
export default {
    name: 'leaderBoardComp',
    data() {
        return {
            beansData: []
        }
    },
    mounted() {
        let URL = 'http://yapa-main-861829938.cn-north-1.elb.amazonaws.com.cn:9999/award/list?actCode=topUp_202403';
        axios.get(URL).
            then((response) => {
                console.log('response.data...???', response.data);
                this.beansData = response.data.data;
                console.log('this.beansData...', this.beansData);
            })
            .catch(err => {
                console.log('fetching data is getting error:', err);
            });
    }
}

</script>

<style lang="less" scoped>
.leaderBoard {
    background-color: #FCF9ED;
    width: 350px;
    height: 591px;
    margin: 0 auto;
    border-radius: 2vw;
    position: relative;
    top: 12vw;
}

.text_14 {
    position: relative;
    width: 317px;
    height: 34px;
    overflow-wrap: break-word;
    color: #e50016;
    font-size: 14px;
    font-family: Roboto-Medium;
    font-weight: 500;
    text-align: center;
    line-height: 20px;
    display: block;
    margin: 0 auto;
    top: 9vw;
}

.welcome-title {
    width: 189px;
    height: 36px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
    top: 68px;
    background: url(../assets/images/picture_title.png);
    background-size: cover;

    h2 {
        position: absolute;
        left: 13vw;
        font-family: Baloo;
        font-size: 16px;
        top: 2vw;
        color: white;
        font-size: 16px;
        width: 110px;
        height: 11px;
        margin: 0 auto;
    }
}

.leaderBoard-strip {
    background: url(../assets/images/strip.png) center/ 100% 100% no-repeat;
    height: 61px;
    width: 330px;
    margin: 7px auto;
    position: relative;
    top: 15vw;
}

.beans-icon {
    display: flex;
    flex-direction: column;
    width: 55px;
    height: 61px;
    gap: 12px;
    align-items: center;
    justify-content: flex-end;

    .beans-img {
        width: 18px;
        height: 20px;
    }

    img {
        width: 100%;
    }

    span {
        width: 24px;
        height: 9px;
        color: #99410C;
    }

    .beans-text {
        width: 100%;
        text-align: center;
        padding: 5px 0 7px 0;
        background: #FFE4BD;
        border-bottom-left-radius: 1vw;
    }
}


.img-container {
    display: flex;
    position: relative;
    top: -55px;
    left: 61px;
    column-gap: 13px;

    .first-icon {
        width: 43px;
        height: 43px;
        background: url(../assets/images/icon-rectangle.png) center/ 100% 100% no-repeat;

        span {
            position: absolute;
            background: white;
            color: #99410C;
            padding: 2px 4px;
            font-size: 8px;
            font-family: Roboto;
            left: 7%;
            border-radius: 8px;
            top: -11%;
            border: 1px solid #FFA234;
            width: 14px;
        }

        img {
            width: 100%;
        }
    }

    .second-icon {
        width: 43px;
        height: 43px;
        background: url(../assets/images/icon-rectangle.png) center/ 100% 100% no-repeat;

        img {
            width: 90%;
            margin: 14px auto;
        }

        span {
            position: absolute;
            background: white;
            color: #99410C;
            padding: 2px 4px;
            font-size: 8px;
            font-family: Roboto;
            left: 22%;
            border-radius: 8px;
            top: -11%;
            border: 1px solid #FFA234;
        }
    }

    .third-icon {
        width: 43px;
        height: 43px;
        background: url(../assets/images/icon-rectangle.png) center/ 100% 100% no-repeat;

        img {
            width: 90%;
            margin: 14px auto;
        }

        span {
            position: absolute;
            background: white;
            color: #99410C;
            padding: 2px 4px;
            font-size: 8px;
            font-family: Roboto;
            left: 39%;
            border-radius: 8px;
            top: -11%;
            border: 1px solid #FFA234;
        }
    }

    .fourth-icon {
        width: 43px;
        height: 43px;
        background: url(../assets/images/icon-rectangle.png) center/ 100% 100% no-repeat;

        img {
            width: 90%;
            margin: -1px auto;
            height: 45px;
        }

        span {
            position: absolute;
            background: white;
            color: #99410C;
            padding: 2px 4px;
            font-size: 8px;
            font-family: Roboto;
            left: 56%;
            border-radius: 8px;
            top: -11%;
            border: 1px solid #FFA234;
        }
    }

    .fifth-icon {
        width: 43px;
        height: 43px;
        background: url(../assets/images/icon-rectangle.png) center/ 100% 100% no-repeat;

        img {
            width: 90%;
            margin: -1px auto;
            height: 45px;
        }

        span {
            position: absolute;
            background: white;
            color: #99410C;
            padding: 2px 4px;
            font-size: 8px;
            font-family: Roboto;
            left: 73%;
            border-radius: 8px;
            top: -11%;
            border: 1px solid #FFA234;
        }
    }
}

.paragraph_1 {
    width: 303px !important;
    height: 40px !important;
    overflow-wrap: break-word;
    color: rgba(153, 65, 12, 1);
    font-size: 10px;
    font-family: Roboto-Regular;
    font-weight: normal;
    text-align: center;
    margin: 10px auto;
    text-align: center;
    margin-top: 2.5rem;
}

.top-up {
    width: 90%;
    height: 12vh;
    margin: 0 auto;

    img {
        width: 100%;
    }
}

.text_2 {
    width: 350px;
    height: 22px;
    overflow-wrap: break-word;
    color: rgba(255, 255, 255, 1);
    font-size: 14px;
    font-family: Roboto-Regular;
    font-weight: normal;
    text-align: center;
    white-space: wrap;
    margin: 0 auto;
}


.line {
    margin: 0 auto;
    color: white;
}

.rights {
    font-size: 14px;
    color: white;
    margin: 0 auto;
}

.footer {
    display: flex;
    flex-direction: column;
}

.num {
    color: yellow;
}
</style>