<template>
    <div class="leaderBoard">
        <span class="text_14">Welcome&nbsp;to&nbsp;YAPA!&nbsp;Start&nbsp;your&nbsp;first&nbsp;topup&nbsp;with&nbsp;more&nbsp;suprising&nbsp;rewards!</span>
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
    top: 9vw;
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
    top: 3vw;
    // margin: 73px 0 0 34px;
    // margin: 0 auto;
}
</style>