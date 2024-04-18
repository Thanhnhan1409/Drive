<script setup lang="ts">
import { Icon } from '@iconify/vue'
import { ref } from 'vue'


const searchValue = ref<string>('')
const valueSwitch = ref<boolean>(false)
const dialogFormVisible = ref<boolean>(false)
function displayFilterPro() {
    dialogFormVisible.value = true
}
</script>

<template>
    <div :class="$style.headerContainer">
        <FilterPro :dialog-form-visible="dialogFormVisible" />
        <div :class="$style.headerLeft">
            <div :class="$style.headerInfor">
                <Icon :class="$style.headerLogo" icon="logos:google-drive" />
                <span :class="$style.headerWebName">Drive</span>
            </div>
            <div :class="$style.headerSearchBox">
                <Icon :class="[$style.headerIcon, $style.headerLookIcon]" icon="material-symbols:search" />
                <input v-model="searchValue" placeholder="Tìm trong Drive" :class="$style.headerInput" type="text">
                <div :class="$style.headerSearchIconGroup">
                    <Icon v-show="searchValue" @click="searchValue = ''" :class="$style.headerIcon" icon="gravity-ui:xmark" />
                    <img :class="$style.headerIcon" @click="displayFilterPro" src="../../assets/images/filter.png" alt="">
                </div>
            </div>
        </div>

        <div :class="$style.headerRight">
            <el-popover placement="bottom-end" :width="300" trigger="click">
                <template #reference>
                    <Icon :class="$style.headerIcon" icon="teenyicons:tick-circle-outline" />
                </template>
                <span :class="$style.headerTickContent">Xem trước khi không có mạng</span>
                <el-switch v-model="valueSwitch" size="small" />
            </el-popover>
            <el-popover placement="bottom-end" :width="280" trigger="click">
                <template #reference>
                    <Icon :class="$style.headerIcon" icon="ant-design:question-circle-outlined" />
                </template>
                <ul>
                    <li :class="$style.headerQuestionItem">Trợ giúp</li>
                    <li :class="$style.headerQuestionItem">Đào tạo</li>
                    <el-divider />
                    <li :class="$style.headerQuestionItem">Điều khoản và chính sách</li>
                    <el-divider />
                    <li :class="$style.headerQuestionItem">Gửi ý kiến phản hồi cho Google</li>
                </ul>
            </el-popover>
            <el-popover placement="bottom-end" :width="320" trigger="click">
                <template #reference>
                    <Icon :class="$style.headerIcon" icon="material-symbols:settings-outline-rounded" />
                </template>
                <ul>
                    <li :class="$style.headerSettingItem">Cài đặt</li>
                    <li :class="$style.headerSettingItem">Tải Drive cho máy tính</li>
                    <li :class="$style.headerSettingItem">Phím tắt</li>
                </ul>
            </el-popover>
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

.headerSettingOptions {
    width: 300px;
}

.headerSettingItem {
    padding: 6px 30px;
    &:hover {
        background-color: #e7e8e9;
    }
}

.headerQuestionItem {
    width: 260px;
    list-style: none;
    cursor: pointer;
    display: block;
    color: #202124;
    font-size: 14px;
    font-weight: 400;
    letter-spacing: .2px;
    line-height: 20px;
    outline: none;
    padding: 6px 10px;

    &:hover {
        background-color: #E7E8EB;
    }
}

:global(.el-popover.el-popper) {
    padding: 6px 0;
}

:global(.el-divider--horizontal) {
    margin: 7px 0;
}

.headerTickContent {
    padding: 6px 30px;
}
</style>
