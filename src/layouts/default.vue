<script setup lang="ts">

</script>

<template>
  <el-container>
    <el-header style="padding: 0;"><Header /></el-header>
    <el-container>
      <el-aside>
        <Sidebar />
      </el-aside>
      <el-main>
        <RouterView />
      </el-main>
    </el-container>
  </el-container>
  </template>
