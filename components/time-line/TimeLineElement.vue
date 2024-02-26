<script setup lang="ts">

interface TimeLineElementPropsModel {
    date: string;
    message: string;
    imageName: string;
}

const { date, message, imageName } = defineProps<TimeLineElementPropsModel>();
</script>

<template>
    <div class="time-line-element" :class="{ 'left': imageName == 'wsiz.png', 'right': imageName == 'ideo.png' }">
        <div class="time-line-pipe">
            <span class="time-line-pipe-text">
                {{ date }}
            </span>
        </div>
        <div class="time-line-card">
            <img class="icon" :src="`/images/${imageName}`" />
            <span class="message">
                {{ message }}
            </span>
        </div>
    </div>
</template>

<style scoped lang="scss">
.time-line-element {
    display: flex;
    justify-content: center;
    width: 100%;
    position: relative;
    margin-top: 40px;

    &.left {
        width: 50%;
        align-self: flex-start;
        margin-left: 49px;

        .time-line-pipe {
            position: absolute;
            inset: 0;
            top: -30px;
            bottom: 0px;
            left: calc(96%);

            .time-line-pipe-text {
                transform: rotate(90deg);
                left: 0px;
            }
        }
    }

    &.right {
        width: 50%;
        align-self: flex-end;
    }

    .time-line-pipe {
        position: absolute;
        width: 7px;
        height: calc(130% + 20px);
        left: 35px;
        top: -30px;
        background-color: black;

        &::after {
            content: '';
            height: 15px;
            width: 15px;
            position: absolute;
            border-radius: 50%;
            top: -4px;
            left: -4px;
            background-color: black;
            z-index: 2;
        }

        .time-line-pipe-text {
            transform: rotate(270deg);
            position: absolute;
            left: -38px;
            top: 45%;
            font-weight: 600;
            font-family: var(--font-base);
            font-size: 20px;
        }
    }

    .time-line-card {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        background-color: hsla(160, 52%, 71%, .05);
        backdrop-filter: 20px;
        margin-left: 30px;
        width: calc(100% - 90px);
        border-radius: 14px;
        padding: 10px 20px;
        gap: 20px;
        -webkit-box-shadow: 0px 0px 3px 0.3px rgba(255, 255, 255, 1);
        -moz-box-shadow: 0px 0px 3px 0.3px rgba(255, 255, 255, 1);
        box-shadow: 0px 0px 3px 0.3px rgba(255, 255, 255, 1);

        .icon {
            height: 40px;
            width: 40px;
            object-fit: cover;
        }

        .message {
            font-weight: 600;
            font-family: var(--font-base);
            color: white;
            word-wrap: normal;
            word-break: keep-all;
            word-spacing: normal;
            text-wrap: pretty;
        }
    }
}
</style>