<script setup lang="ts">

const item = {
  type: 0,
  title: 'Information OOP',
  user :{
    type: 1,
    name: 'nhan',
    avt:  'https://scontent.fdad3-6.fna.fbcdn.net/v/t39.30808-6/359769371_1313465892581025_7630482997321218589_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5f2048&_nc_eui2=AeEpBKwzTGVPxu0BwrzxgStafT6-QUHpGlR9Pr5BQekaVMZffx6DTDBImzhfWgnTqVYornfUPvzVVXPq96H23Pcp&_nc_ohc=B_m_j64Q5KYAb6HowVF&_nc_ht=scontent.fdad3-6.fna&oh=00_AfBeXDYa6o9xzJ0XDR6e0aiARmp4PJmUTdn9Xryej40PFA&oe=66268C93'
  },
  lastEdit: '15-04-2024',
  fileSize: '123'
}
</script>

<template>
  <div>
    <h1>Hello World</h1>
    <ElButton>
      Hehe
    </ElButton>
    <FileExplorerItem :item="item"/>
  </div>
</template>
