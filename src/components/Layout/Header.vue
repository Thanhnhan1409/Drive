<script setup lang="ts">
import { Icon } from '@iconify/vue'
import { ref } from 'vue'

const searchValue = ref<string>('')
</script>

<template>
    <div :class="$style.headerContainer">
        <div :class="$style.headerLeft">
            <div :class="$style.headerInfor">
                <Icon :class="$style.headerLogo" icon="logos:google-drive" />
                <span :class="$style.headerWebName">Drive</span>
            </div>
            <div :class="$style.headerSearchBox">
                <Icon :class="[$style.headerIcon, $style.headerLookIcon]" icon="material-symbols:search" />
                <input v-model="searchValue" placeholder="Tìm trong Drive" :class="$style.headerInput" type="text">
                <div :class="$style.headerSearchIconGroup">
                    <Icon v-show="searchValue" :class="$style.headerIcon" icon="gravity-ui:xmark" />
                    <img :class="$style.headerIcon" src="../../assets/images/filter.png" alt="">
                    <!-- <Icon icon="material-symbols:filter-alt-outline" /> -->
                </div>
            </div>
        </div>

        <div :class="$style.headerRight">
            <Icon :class="$style.headerIcon" icon="teenyicons:tick-circle-outline" />
            <Icon :class="$style.headerIcon" icon="ant-design:question-circle-outlined" />
            <Icon :class="$style.headerIcon" icon="material-symbols:settings-outline-rounded" />
            <Icon :class="$style.headerIcon" icon="material-symbols:apps" />
            <img :class="$style.headerAvt" src="../../assets/images/avt.jpg" alt="avatar">
        </div>
    </div>
</template>

<style module lang="scss">
.headerContainer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 8px;
    background-color: #F8FAFD;
}

.headerLeft {
    display: flex;
    align-items: center;
    gap: 20px;
    width: 80%;
}

.headerInfor {
    display: flex;
    align-items: center;
    width: 226px;
}

.headerLogo {
    width: 40px;
    height: 36px;
    margin-bottom: 4px;
    margin-left: 14px;
    padding: 2px;
}

.headerWebName {
    display: inline-block;
    font-size: 22px;
    line-height: 24px;
    padding-left: 8px;
}

.headerSearchBox {
    position: relative;
    min-width: 550px;
    width: 60%;
}

.headerInput {
    padding: 16px 100px 16px 60px;
    border: none;
    border-radius: 26px;
    width: 100%;
    background-color: #E9EEF6;

    &:focus {
        background-color: #ffff;
        outline: none;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
    }
}

.headerSearchIconGroup {
    display: flex;
    align-items: center;
    gap: 2px;
    position: absolute;
    top: 1.5px;
    right: 5px;
}

.headerRight {
    display: flex;
    align-items: center;
}

.headerIcon {
    width: 24px;
    height: 24px;
    padding: 8px;
    box-sizing: content-box;
    margin: 2px;
    border-radius: 50%;

    &:hover {
        background-color: rgb(230, 233, 235);
    }
}

.headerLookIcon {
    position: absolute;
    top: 1.5px;
    left: 5px;
}

.headerAvt {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    box-sizing: content-box;
    padding: 4px;
    margin: 2px;
    object-fit: contain;

    &:hover {
        background-color: #e7e8e9;
    }
}
</style>