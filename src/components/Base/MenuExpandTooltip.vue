<script setup lang="ts">
import { Icon } from '@iconify/vue'

const menuExpandItems = [
    {
        id: 1,
        icon: 'material-symbols:open-with-rounded',
        label: 'Mở bằng',
        expand: true
    },
    {
        id: 2,
        icon: 'material-symbols-light:download-rounded',
        label: 'Tải xuống'
    },
    {
        id: 3,
        icon: 'solar:pen-2-outline',
        label: 'Đổi tên'
    },
    {
        id: 4,
        icon: 'line-md:account-add',
        label: 'Chia sẻ',
        expand: true
    },
    {
        id: 5,
        icon: 'material-symbols-light:folder-open',
        label: 'Sắp xếp',
        expand: true
    },
    {
        id: 6,
        icon: 'f7:exclamationmark-circle',
        label: 'Thông tin về thư mục',
        expand: true
    },
    {
        id: 7,
        icon: 'uil:trash-alt',
        label: 'Chuyển vào thùng rác'
    }
]
</script>

<template>
    <el-popover placement="bottom-end" :width="300" trigger="click">
            <template #reference>
                <Icon :class="$style.fileItemIcon" icon="ph:dots-three-outline-vertical-fill" />
            </template>
            <div>
                <div v-for="item in menuExpandItems" :key="item.id">
                    <div :class="$style.fileItemExpandItem">
                        <div :class="$style.fileItemExpandItemFirst">
                            <Icon :class="$style.fileItemExpandIcon" :icon="item.icon" />
                            <span>{{ item.label }}</span>
                        </div>
                        <Icon :class="$style.fileItemExpandIcon" v-show="item.expand" icon="ic:baseline-arrow-right" />
                    </div>
                    <el-divider v-show="item.id === 1 || item.id === 3 || item.id === 6" />
                </div>
            </div>
        </el-popover>
</template>

<style module lang="scss">
.fileItemIcon {
    width: 16px;
    height: 16px;
    padding: 10px;
    box-sizing: content-box;
    cursor: pointer;
    margin: 2px;
    border-radius: 50%;

    &:hover {
        background-color: #E7E8EB;
    }
}

.fileItemExpandItem {
    list-style: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: space-between;
    color: #202124;
    font-size: 14px;
    font-weight: 400;
    letter-spacing: .2px;
    line-height: 20px;
    outline: none;
    padding: 6px 15px;

    &:hover {
        background-color: #e7e8e9;
    }
}

.fileItemExpandItemFirst {
    display: flex;
    align-items: center;
    gap: 15px;
}

.fileItemExpandIcon {
    width: 20px;
    height: 20px;
}
</style>