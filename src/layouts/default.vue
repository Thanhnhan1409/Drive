<script setup lang="ts">

</script>

<template>
  <el-container>
    <el-header style="padding: 0;">
      <Header />
    </el-header>
    <el-container>
      <div :class="$style.layoutSidebar">
        <Sidebar />
      </div>
      <el-main :class="$style.layoutMain">
        <RouterView />
      </el-main>
    </el-container>
  </el-container>
</template>

<style module lang="scss">
.layoutMain {
  border-radius: 16px;
}
</style>