<script setup>
// import log from './pages/log.vue'
import { ref } from 'vue'
// 存储basicbox的内容
const basicBoxes = ref([
    'awd1',
    'awd2',
    'awd3',
])

const addBasicBox = () => {
    basicBoxes.value.push('new box');
}
</script>

<template>
    <!-- <log /> -->
    <div class="mainbox">
        <div class="header">
            <div class="logo">
                <a href="#">
                    <img src="./assets/imgs/me.jpg" alt="">
                </a>
            </div>
            <div class="content">
                <div class="title">
                    <span class="time">morning</span> ! <span class="name">world</span> . It's <span
                        class="weather">sunny</span> today, <span class="action"> so let's go for a walk </span>
                </div>
            </div>
        </div>
        <div class="memobox">
            <div v-for="(content, index) in basicBoxes" :key="index" class="basicbox">
                {{ content }}
            </div>
            <button class="initbox">
                <div class="init-content">
                    <svg t="1724579529135" class="icon" viewBox="0 0 1024 1024" version="1.1"
                        xmlns="http://www.w3.org/2000/svg" p-id="1397" width="2dvw">
                        <path
                            d="M512 0c282.7776 0 512 229.2224 512 512s-229.2224 512-512 512S0 794.7776 0 512 229.2224 0 512 0z m0 61.44a450.56 450.56 0 1 0 0 901.12 450.56 450.56 0 0 0 0-901.12z m0 220.16a30.72 30.72 0 0 1 30.72 30.72v174.08h168.96a30.72 30.72 0 0 1 0 61.44l-168.96-0.0512V711.68a30.72 30.72 0 0 1-61.44 0v-163.8912l-168.96 0.0512a30.72 30.72 0 0 1 0-61.44l168.9088-0.0512L481.28 312.32a30.72 30.72 0 0 1 30.72-30.72z"
                            fill="rgb(202, 202, 202,1)" p-id="1398"></path>
                    </svg>
                    <div class="init-text" @click="addBasicBox">
                        add a new memo
                    </div>
                </div>
            </button>
        </div>
    </div>
</template>

<style scoped lang="less">
.mainbox {
    width: 100dvw;
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    .header {
        width: 95dvw;
        margin-top: 3dvh;
        display: flex;
        align-items: center;

        .logo {
            width: 5dvw;

            img {
                width: 5dvw;
                border-radius: 10px;
            }
        }

        .content {
            padding: 1dvw;
            margin-left: 1.5dvw;
            height: 100%;
            width: auto;

            .title {
                color: rgb(255, 255, 255);
                font-family: ub;
                font-size: 2dvw;

                .time {
                    color: rgb(0, 173, 95);
                }

                .weather {
                    color: rgb(0, 80, 200)
                }
            }
        }
    }

    .memobox {
        margin-top: 3dvh;
        width: 85dvw;
        height: auto;
        min-height: 20dvh;
        padding: 5dvw;
        border-radius: 10px;
        background-color: rgba(0, 0, 0, 0.158);
        display: flex;
        flex-wrap: wrap;

        .initbox {
            cursor: pointer;
            border:solid;
            border-color: #00c192;
            height: 20dvh;
            width: 21%;
            margin: 1% 2%;
            background-color: rgb(51, 51, 51);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            .init-content{
                display: flex;
                flex-direction: column;
                align-items: center;
                .init-text{
                    margin-top: 1dvh;
                    color: rgb(202, 202, 202,1);
                    font-size: 0.8dvw;
                    font-family: ub;
                }
            }
        }

        .basicbox {
            height: 20dvh;
            width: 21%;
            min-width: 15%;
            min-height: 15dvh;
            max-width: 45%;
            max-height: 30dvh;
            margin: 1% 2%;
            background-color: rgb(40, 40, 40);
            border-radius: 8px;
            display: flex;
            resize: both;
            overflow: hidden;
            &::-webkit-resizer {
                background-color: #00c192;
                border-radius: 50%;
            }
        }
    }
}
</style>
