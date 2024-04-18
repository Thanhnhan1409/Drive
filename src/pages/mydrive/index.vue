
<script lang="ts" setup>
import { Icon } from '@iconify/vue'

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
</script>

<template>
    <div>
        <div>
            <h1>Drive của tôi</h1>
            <div>
                
            </div>
        </div>
        <div></div>
        <div :class="$style.mydriveTitle">
            <span :class="$style.mydriveName">Tên</span>
            <span :class="$style.mydriveOwner">Chủ sở hữu</span>
            <span :class="$style.mydriveLastEdit">Do tôi sửa gần đây</span>
            <span :class="$style.mydriveFileSize">Kích cỡ tệp</span>
            <Icon icon="bi:three-dots-vertical" />
        </div>
        <div>
            <FileExplorerItem v-for="(item, index) in data" :key="index" :item="item"/>
            </div>
        </div>
</template>

<style module lang="scss">
.mydriveTitle {
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

    &:hover {
        background-color: #e7e8e9;
    }
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
.fileItemExpandItemFirst {
    display: flex;
    align-items: center;
    gap: 15px;
}
</style>