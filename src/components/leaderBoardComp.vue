<template>
    <div class="welcome-title">
        <img src="../assets/images/picture_title.png" alt="welcom">
    </div>
    <div class="leaderBoard">
        <span
            class="text_14">Welcome&nbsp;to&nbsp;YAPA!&nbsp;Start&nbsp;your&nbsp;first&nbsp;topup&nbsp;with&nbsp;more&nbsp;suprising&nbsp;rewards!</span>
        <div class="leaderBoard-strip">
            <div class="beans-icon">
                <img src="../assets/images/beans-icon.png" alt="beans">
                <span>1000</span>
            </div>

            <div class="img-container">
                <div class="left-icon">
                    <img src="../assets/images/group-beans.png" alt="groupbeans">
                </div>
                <div class="right-icon">
                    <img src="../assets/images/wallet.png" alt="groupbeans">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'leaderBoardComp',
}

</script>

<style lang="less" scoped>
.leaderBoard {
    background-color: #FCF9ED;
    width: 90%;
    height: 70vh;
    margin: 0 auto;
    border-radius: 2vw;
    position: relative;
    top: -20vw;
    // bottom: -10rem;
}

.text_14 {
    position: relative;
    width: 81vw;
    height: 68px;
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
    // margin: 73px 0 0 34px;
    // margin: 0 auto;
}

.welcome-title {
    width: 70%;
    height: 50%;
    margin: 10vw auto;
    position: relative;
    z-index: 1;

    img {
        width: 100%;
    }
}

.leaderBoard-strip {
    background: url(../assets/images/strip.png);
    height: 13vh;
    width: 100%;
    // opacity: 100;
    background-size: cover;
    background-size: 100% 100%;

    // background-color: rgba(0, 10, 0, 100);
}

.beans-icon {
    display: flex;
    flex-direction: column;
    width: 10%;
    gap: 3vw;

    img {
        width: 100%;
    }

    span {
        width: 10%;
    }
}


.img-container {
    display: flex;
    justify-content: space-evenly;
    position: relative;
    top: -3.5rem;

    .left-icon {
        width: 20%;
        height: 12vh;
        background: url(../assets/images/icon-rectangle.png);
        background-size: cover;
        background-size: 100% 100%;

        img {
            width: 100%;
        }
    }

    .right-icon {
        width: 20%;
        height: 12vh;
        background: url(../assets/images/icon-rectangle.png);
        background-size: cover;
        background-size: 100% 100%;
        img {
            width: 90%;
            margin: 0 auto;
        }
    }
}




// .leaderBoard-strip {
//     content: "";
//     // position: absolute;
//     top: 0;
//     left: 0;
//     width: 100%;
//     height: 100%;
//     background-color: rgba(0, 0, 0, 0.5); /* Adjust opacity here (0.5 is 50% opacity) */
// }</style>