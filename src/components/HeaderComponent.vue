<template>
    <div>
        <!-- open the modal component button -->
        <div class="header">
            <div class="float_rules">
                <button @click="openRulesTab">Rules</button>
            </div>
        </div>

        <!-- modal component -->
        <div class="modal" v-if="isModalOpen">
            <div class="modal-content">
                <span class="close" @click="closeModal">&times;</span>
                <!-- Rules content goes here -->
                <h2>Rules</h2>
                <p>Put your rules content here...</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data() {
        this.isModalOpen = false;
    },
    methods: {
        openRulesTab() {
            this.isModalOpen = true;
            console.log('openRulse tab open');
        },
        closeModal() {
            this.isModalOpen = false;
        }
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
}
</style>