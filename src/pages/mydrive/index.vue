
<script lang="ts" setup>
import { Icon } from '@iconify/vue'
import { ref } from 'vue';

const data = [
    {
        type: 0,
        title: 'Information OOP',
        user: {
            type: 1,
            name: 'nhan',
            avt: 'https://scontent.fdad3-6.fna.fbcdn.net/v/t39.30808-6/359769371_1313465892581025_7630482997321218589_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeEpBKwzTGVPxu0BwrzxgStafT6-QUHpGlR9Pr5BQekaVMZffx6DTDBImzhfWgnTqVYornfUPvzVVXPq96H23Pcp&_nc_ohc=B_m_j64Q5KYAb6HowVF&_nc_ht=scontent.fdad3-6.fna&oh=00_AfBeXDYa6o9xzJ0XDR6e0aiARmp4PJmUTdn9Xryej40PFA&oe=66268C93'
        },
        lastEdit: '15-04-2024',
        fileSize: '123'
    },
    {
        type: 0,
        title: 'Information OOP',
        user: {
            type: 1,
            name: 'nhan',
            avt: 'https://scontent.fdad3-6.fna.fbcdn.net/v/t39.30808-6/359769371_1313465892581025_7630482997321218589_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeEpBKwzTGVPxu0BwrzxgStafT6-QUHpGlR9Pr5BQekaVMZffx6DTDBImzhfWgnTqVYornfUPvzVVXPq96H23Pcp&_nc_ohc=B_m_j64Q5KYAb6HowVF&_nc_ht=scontent.fdad3-6.fna&oh=00_AfBeXDYa6o9xzJ0XDR6e0aiARmp4PJmUTdn9Xryej40PFA&oe=66268C93'
        },
        lastEdit: '15-04-2024',
        fileSize: '123'
    },
    {
        type: 0,
        title: 'Information OOP',
        user: {
            type: 1,
            name: 'nhan',
            avt: 'https://scontent.fdad3-6.fna.fbcdn.net/v/t39.30808-6/359769371_1313465892581025_7630482997321218589_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeEpBKwzTGVPxu0BwrzxgStafT6-QUHpGlR9Pr5BQekaVMZffx6DTDBImzhfWgnTqVYornfUPvzVVXPq96H23Pcp&_nc_ohc=B_m_j64Q5KYAb6HowVF&_nc_ht=scontent.fdad3-6.fna&oh=00_AfBeXDYa6o9xzJ0XDR6e0aiARmp4PJmUTdn9Xryej40PFA&oe=66268C93'
        },
        lastEdit: '15-04-2024',
        fileSize: '123'
    },
    {
        type: 0,
        title: 'Information OOP',
        user: {
            type: 1,
            name: 'nhan',
            avt: 'https://scontent.fdad3-6.fna.fbcdn.net/v/t39.30808-6/359769371_1313465892581025_7630482997321218589_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeEpBKwzTGVPxu0BwrzxgStafT6-QUHpGlR9Pr5BQekaVMZffx6DTDBImzhfWgnTqVYornfUPvzVVXPq96H23Pcp&_nc_ohc=B_m_j64Q5KYAb6HowVF&_nc_ht=scontent.fdad3-6.fna&oh=00_AfBeXDYa6o9xzJ0XDR6e0aiARmp4PJmUTdn9Xryej40PFA&oe=66268C93'
        },
        lastEdit: '15-04-2024',
        fileSize: '123'
    },
    {
        type: 0,
        title: 'Information OOP',
        user: {
            type: 1,
            name: 'nhan',
            avt: 'https://scontent.fdad3-6.fna.fbcdn.net/v/t39.30808-6/359769371_1313465892581025_7630482997321218589_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeEpBKwzTGVPxu0BwrzxgStafT6-QUHpGlR9Pr5BQekaVMZffx6DTDBImzhfWgnTqVYornfUPvzVVXPq96H23Pcp&_nc_ohc=B_m_j64Q5KYAb6HowVF&_nc_ht=scontent.fdad3-6.fna&oh=00_AfBeXDYa6o9xzJ0XDR6e0aiARmp4PJmUTdn9Xryej40PFA&oe=66268C93'
        },
        lastEdit: '15-04-2024',
        fileSize: '123'
    },
    {
        type: 0,
        title: 'Information OOP',
        user: {
            type: 1,
            name: 'nhan',
            avt: 'https://scontent.fdad3-6.fna.fbcdn.net/v/t39.30808-6/359769371_1313465892581025_7630482997321218589_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeEpBKwzTGVPxu0BwrzxgStafT6-QUHpGlR9Pr5BQekaVMZffx6DTDBImzhfWgnTqVYornfUPvzVVXPq96H23Pcp&_nc_ohc=B_m_j64Q5KYAb6HowVF&_nc_ht=scontent.fdad3-6.fna&oh=00_AfBeXDYa6o9xzJ0XDR6e0aiARmp4PJmUTdn9Xryej40PFA&oe=66268C93'
        },
        lastEdit: '15-04-2024',
        fileSize: '123'
    }, {
        type: 0,
        title: 'Information OOP',
        user: {
            type: 1,
            name: 'nhan',
            avt: 'https://scontent.fdad3-6.fna.fbcdn.net/v/t39.30808-6/359769371_1313465892581025_7630482997321218589_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeEpBKwzTGVPxu0BwrzxgStafT6-QUHpGlR9Pr5BQekaVMZffx6DTDBImzhfWgnTqVYornfUPvzVVXPq96H23Pcp&_nc_ohc=B_m_j64Q5KYAb6HowVF&_nc_ht=scontent.fdad3-6.fna&oh=00_AfBeXDYa6o9xzJ0XDR6e0aiARmp4PJmUTdn9Xryej40PFA&oe=66268C93'
        },
        lastEdit: '15-04-2024',
        fileSize: '123'
    }, {
        type: 0,
        title: 'Information OOP',
        user: {
            type: 1,
            name: 'nhan',
            avt: 'https://scontent.fdad3-6.fna.fbcdn.net/v/t39.30808-6/359769371_1313465892581025_7630482997321218589_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeEpBKwzTGVPxu0BwrzxgStafT6-QUHpGlR9Pr5BQekaVMZffx6DTDBImzhfWgnTqVYornfUPvzVVXPq96H23Pcp&_nc_ohc=B_m_j64Q5KYAb6HowVF&_nc_ht=scontent.fdad3-6.fna&oh=00_AfBeXDYa6o9xzJ0XDR6e0aiARmp4PJmUTdn9Xryej40PFA&oe=66268C93'
        },
        lastEdit: '15-04-2024',
        fileSize: '123'
    }
]
const activeElement = ref<number>(0)
</script>

<template>
    <div>
        <div :class="$style.mydriveTitleBox">
            <h1 :class="$style.mydriveTitle">Drive của tôi</h1>
            <div :class="$style.mydriveOptionsBox">
                <div :class="$style.mydriveDisplayOptions">
                    <div 
                        :class="activeElement === 0 && $style.mydriveActiveOption"
                        @click="activeElement = 0">
                        <Icon v-show="activeElement === 0" icon="clarity:success-line" />
                        <Icon icon="fluent:navigation-16-filled" />
                    </div>
                    <div
                        :class="activeElement === 1 && $style.mydriveActiveOption"
                        @click="activeElement = 1">
                        <Icon v-show="activeElement === 1" icon="clarity:success-line" />
                        <Icon icon="octicon:apps-16" />
                    </div>
                </div>
                <Icon :class="$style.mydriveTitleIcon" icon="f7:exclamationmark-circle" />
            </div>
        </div>
        <div :class="$style.mydriveDropdownGroup">
            <el-dropdown trigger="click" placement="bottom-end">
                <span class="el-dropdown-link">
                    Loại
                    <Icon icon="material-symbols:arrow-drop-down-rounded" />
                </span>
                <template #dropdown>
                    <el-dropdown-menu>
                        <el-dropdown-item command="a">Action 1</el-dropdown-item>
                        <el-dropdown-item command="b">Action 2</el-dropdown-item>
                        <el-dropdown-item command="c">Action 3</el-dropdown-item>
                        <el-dropdown-item command="d" disabled>Action 4</el-dropdown-item>
                        <el-dropdown-item command="e" divided>Action 5</el-dropdown-item>
                    </el-dropdown-menu>
                </template>
            </el-dropdown>
            <el-dropdown trigger="click" placement="bottom-end">
                <span class="el-dropdown-link">
                    Người
                    <Icon icon="material-symbols:arrow-drop-down-rounded" />
                </span>
                <template #dropdown>
                    <el-dropdown-menu>
                        <el-dropdown-item command="a">Action 1</el-dropdown-item>
                        <el-dropdown-item command="b">Action 2</el-dropdown-item>
                        <el-dropdown-item command="c">Action 3</el-dropdown-item>
                        <el-dropdown-item command="d" disabled>Action 4</el-dropdown-item>
                        <el-dropdown-item command="e" divided>Action 5</el-dropdown-item>
                    </el-dropdown-menu>
                </template>
            </el-dropdown>
            <el-dropdown trigger="click" placement="bottom-end">
                <span class="el-dropdown-link">
                    Lần sửa đổi gần đây nhất
                    <Icon icon="material-symbols:arrow-drop-down-rounded" />
                </span>
                <template #dropdown>
                    <el-dropdown-menu>
                        <el-dropdown-item command="a">Hôm nay</el-dropdown-item>
                        <el-dropdown-item command="b">7 ngày qua</el-dropdown-item>
                        <el-dropdown-item command="c">30 ngày qua</el-dropdown-item>
                        <el-dropdown-item command="d">Năm nay</el-dropdown-item>
                        <el-dropdown-item command="e">Năm ngoái</el-dropdown-item>
                        <el-dropdown-item command="e">Năm ngoái</el-dropdown-item>
                        <el-dropdown-item command="e">Phạm vi tùy chỉnh</el-dropdown-item>
                        <el-dropdown-item divided command="e">
                            <button :class="$style.mydriveLastEditButton">Xóa tất cả</button>
                            <button :class="$style.mydriveLastEditButton">Hủy</button>
                            <button :class="$style.mydriveLastEditButton">Áp dụng</button>
                        </el-dropdown-item>
                    </el-dropdown-menu>
                </template>
            </el-dropdown>
        </div>
        <div v-if="activeElement === 0" :class="$style.mydriveTitleColumn">
            <span :class="$style.mydriveName">Tên</span>
            <span :class="$style.mydriveOwner">Chủ sở hữu</span>
            <span :class="$style.mydriveLastEdit">Do tôi sửa gần đây</span>
            <span :class="$style.mydriveFileSize">Kích cỡ tệp</span>
            <Icon icon="bi:three-dots-vertical" />
        </div>
        <div v-if="activeElement === 0">
            <FileExplorerItem v-for="(item, index) in data" :key="index" :item="item" />
        </div>
        <div v-else :class="$style.mydriveCardList">
            <FilteExploreCard v-for="(item, index) in data" :key="index" :item="item" />
        </div>
    </div>
</template>

<style module lang="scss">
.mydriveTitleBox {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.mydriveTitle {
    font-size: 28px;
    font-weight: 500;
}

.mydriveOptionsBox {
    display: flex;
    gap: 8px;
}

.mydriveDisplayOptions {
    display: flex;
    align-items: center;
    border-radius: 18px;
    border: 1px solid black;
    overflow: hidden;

    &>div {
        width: 55px;
        padding: 8px;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 4px;
        cursor: pointer;
    }

    &>div:first-child {
        border-right: 1px solid black;
    }
}

.mydriveActiveOption {
    background-color: #C2E7FF;
}

.mydriveTitleIcon {
    width: 34px;
    height: 34px;
    padding: 8px;
    border-radius: 50%;

    &:hover {
        background-color: #e7e8e9;
    }
}

.mydriveTitleColumn {
    list-style: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    color: #202124;
    font-size: 14px;
    font-weight: 400;
    letter-spacing: .2px;
    line-height: 20px;
    outline: none;
    padding: 6px 15px;
    border-bottom: 1px solid rgb(218, 220, 224);
    margin-top: 20px;
}

.mydriveName {
    width: 45%;
}

.mydriveOwner {
    width: 215px;
}

.mydriveFileSize {
    width: 235px;
}

.mydriveLastEdit {
    width: 180px;
}

.mydriveLastEditButton {
    border: none;
    background: #ffff;
    margin-right: 10px;
    padding: 6px 20px;
    border-radius: 22px;
    height: 48px;

    &:hover {
        background-color: #E9EEF6;
        color: #296CD6;
    }
}

.mydriveDropdownGroup {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-top: 20px;
}

:global(.el-dropdown) {
    line-height: 32px;
    border: 1px solid black;
    padding: 0 16px;
    border-radius: 8px;
}

.mydriveCardList {
    margin-top: 20px;
    display: grid;
    grid-gap: 16px;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
}
</style>