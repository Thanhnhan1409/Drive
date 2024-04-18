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
</script>

<template>
    <div :class="$style.fileExploreCard">
        <div :class="$style.fileExploreCardHeader">
            <div :class="$style.fileExploreCardTitle">
                <Icon icon="vscode-icons:file-type-word" />
                <span>{{ item.title }}</span>
            </div>
            <MenuExpandTooltip />
        </div>
        <div :class="$style.fileExploreCardImageBox">
            <img :class="$style.fileExploreCardImage" src="https://bedental.vn/wp-content/uploads/2022/12/659dca8293fc6acd398dac9f564a03bf.jpg" alt="">
        </div>
    </div>
</template>

<style module lang="scss">
.fileExploreCard {
    overflow: hidden;
    height: 300px;
    background-color: #F8FAFD;
    border-radius: 12px;
}

.fileExploreCardHeader {
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: space-between;
    padding: 12px 16px;
}

.fileExploreCardTitle {
    display: flex;
    align-items: center;
    gap: 16px;
}

.fileExploreCardImageBox {
    width: 95%;
    height: 75%;
    background-color: #ffff;
    margin: 0 8px 8px 8px;
    border-radius: 6px;

}

.fileExploreCardImage {
    width: 100%;
    height: 100%;
    object-fit: contain;
}
</style>