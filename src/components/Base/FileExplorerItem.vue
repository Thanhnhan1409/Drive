<script setup lang="ts">
import { Icon } from '@iconify/vue'

interface IFileExplorerItem {
    type: number
    title: string
    user: {
        name: string,
        type: number,
        avt: string
    }
    lastEdit: string
    fileSize?: number
}

defineProps<{
    item: IFileExplorerItem
}>()

function convertDate(date: string) {
    const parts = date.split('-');

    const day = parts[0];
    const month = parts[1];
    const year = parts[2];

    return `${day} thg ${month}, ${year}`;
}
</script>

<template>
    <div :class="$style.fileItemContainer">
        <div :class="$style.fileItemFileIconBox">
            <Icon :class="$style.fileItemFileIcon"
                :icon="item.type === 0 ? 'mdi:file-document' : 'material-symbols:folder'" />
        </div>
        <span :class="$style.fileItemTilte">{{ item.title }}</span>
        <div :class="$style.fileItemUserBox">
            <img :class="$style.fileItemUserAvt" :src="item.user.avt" alt="">
            <span>{{ item.user.type === 0 ? 'Tôi' : item.user.name }}</span>
        </div>
        <span :class="$style.fileItemlastEdit">{{ convertDate(item.lastEdit) }}</span>
        <span v-show="item.fileSize">{{ item.fileSize }}</span>
        <div :class="$style.fileItemButtonGroup">
            <Icon :class="$style.fileItemIcon" icon="lucide:user-plus" />
            <Icon :class="$style.fileItemIcon" icon="mingcute:download-2-line" />
            <Icon :class="$style.fileItemIcon" icon="solar:pen-2-outline" />
            <Icon :class="$style.fileItemIcon" icon="mdi:star-outline" />
        </div>
        <MenuExpandTooltip />
    </div>
</template>

<style module lang="scss">
.fileItemContainer {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 48px;
    line-height: 48px;
    border-bottom: 1px solid rgb(218, 220, 224);

    &:hover {
        background-color: #f8f8f8;
    }

    &:hover .fileItemButtonGroup {
        opacity: 1;
    }
}

.fileItemButtonGroup {
    display: flex;
    align-items: center;
    opacity: 0;
}

.fileItemFileIconBox {
    width: 56px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.fileItemFileIcon {
    width: 24px;
    height: 24px;
}

.fileItemTilte {
    width: calc(45% - 56px);
}

.fileItemlastEdit {
    width: 180px;
}

.fileItemUserBox {
    display: flex;
    align-items: center;
    width: 215px;
    gap: 8px;
}

.fileItemUserAvt {
    width: 30px;
    height: 30px;
    border-radius: 50%;
}

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
</style>