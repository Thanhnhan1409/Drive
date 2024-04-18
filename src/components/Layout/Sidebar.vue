<script setup lang="ts">
import { Icon } from '@iconify/vue'
import { ref } from 'vue'

export interface ISidebarMenu {
  id: number
  title: string
  icon: string
  children?: ISidebarMenu[]
  isCollapse?: boolean
}

const activeItemId = ref<number>(1)
const dataUsed = ref<number>(12)
const dataTree = ref<ISidebarMenu[]>([
  {
    id: 1,
    title: 'Trang chủ',
    icon: 'mdi:home-variant',
  },
  {
    id: 2,
    title: 'Drive của tôi',
    icon: 'mingcute:drive-fill',
    isCollapse: true,
    children: [
      {
        id: 10,
        icon: 'material-symbols-light:folder',
        title: 'BT_SGroup'
      },
      {
        id: 11,
        icon: 'material-symbols-light:folder',
        title: 'OOP'
      },
      {
        id: 12,
        icon: 'material-symbols-light:folder',
        title: 'CTDL'
      },
      {
        id: 13,
        icon: 'material-symbols-light:folder',
        title: 'WorkDoc'
      },
    ]
  },
  {
    id: 3,
    title: 'Máy tính',
    icon: 'fluent:phone-laptop-20-regular',
    isCollapse: true,
  },
  {
    id: 4,
    title: 'Được chia sẻ với tôi',
    icon: 'heroicons:users-20-solid',
  },
  {
    id: 5,
    title: 'Gần đây',
    icon: 'ic:baseline-access-time',
  },
  {
    id: 6,
    title: 'Có gắn dấu sao',
    icon: 'ic:round-star-border',
  },
  {
    id: 7,
    title: 'Nội dung rác',
    icon: 'system-uicons:warning-hex',
  },
  {
    id: 8,
    title: 'Thùng rác',
    icon: 'material-symbols:delete-outline',
  },
  {
    id: 9,
    title: `Bộ nhớ (đã dùng ${dataUsed.value / 15 * 100}%)`,
    icon: 'ic:outline-cloud-queue',
  },
])
const openItemId = ref<number>(0)

function handleClickActiveItem(id: number) {
  activeItemId.value = id
}

function handleExpand(id: number) {
  if (openItemId.value === id)
    openItemId.value = 0;
  else openItemId.value = id;
}
</script>

<template>
  <div :class="$style.sidebarContainer">
    <button :class="$style.sidebarAddButton">
      <Icon :class="$style.sidebarIcon" icon="material-symbols:add-rounded" />
      <span>Mới</span>
    </button>
    <div>
      <div v-for="(item, index) in dataTree" :key="item.id" @click="handleClickActiveItem(item.id)">
        <div
          :class="[$style.sidebarItem, index % 3 === 0 ? $style.sidebarItemSpace : '', item.id === activeItemId ? $style.sidebarActiveItem : '']">
          <Icon @click="handleExpand(item.id)" :class="$style.sidebarItemCollapseIcon"
            :icon="item.isCollapse && item.id === openItemId ? 'material-symbols:arrow-drop-down-rounded' : item.isCollapse ? 'material-symbols:arrow-right' : 'nothing'" />
          <Icon :class="$style.sidebarItemIcon" :icon="item.icon || 'nothing'" />
          <span>{{ item.title }}</span>
        </div>
        <div :class="$style.sidebarChildren" v-show="item.children && item.id === openItemId">
          <div :class="$style.sidebarItem" v-for="subItem in item.children" :key="subItem.id">
            <Icon :class="$style.sidebarItemCollapseIcon"
              :icon="subItem.isCollapse ? 'material-symbols:arrow-right' : 'nothing'" />
            <Icon :class="$style.sidebarItemIcon" :icon="subItem.icon" />
            <span>{{ item.title }}</span>
          </div>
        </div>
      </div>
    </div>
    <div :class="$style.sidebarData">
      <el-progress :stroke-width="4" style="width: 180px;" :percentage="dataUsed / 15 * 100" color="#F09D00"/>
      <p>Đã sử dụng {{ dataUsed }} GB trong tổng số 15 GB</p>
    </div>
    <button :class="$style.sidebarBuyStorageButton">
      Mua thêm bộ nhớ
    </button>
  </div>
</template>

<style module lang="scss">
.sidebarContainer {
  padding: 8px 15px;
  background-color: #F8FAFD;
  width: 256px;
  min-height: 91vh;
  height: 100%;
}

.sidebarAddButton {
  padding: 18px 25px 18px 16px;
  border-radius: 16px;
  background-color: #ffff;
  display: flex;
  align-items: center;
  gap: 12px;
  cursor: pointer;
  border: none;
  box-shadow: rgba(0, 0, 0, 0.3) 0px 4px 6px;

  span {
    font-size: 14px;
  }

  &:hover {
    background-color: #E9EEF6;
  }
}

.sidebarIcon {
  width: 24px;
  height: 24px;
}

.sidebarItem {
  display: flex;
  align-items: center;
  line-height: 32px;
  cursor: pointer;
  border-radius: 16px;
  padding-left: 2px;
  font-size: 14px;

  &:hover {
    background-color: #e7e8e9;
  }
}

.sidebarChildren {
  padding-left: 30px;
}

.sidebarItemSpace {
  margin-top: 16px;
}

.sidebarItemCollapseIcon {
  width: 12px;
  height: 12px;
}

.sidebarItemIcon {
  width: 20px;
  height: 20px;
  margin-right: 14px;
}

.sidebarData {
  padding: 5px 20px 0 16px;

  p {
    font-size: 14px;
    margin-top: 12px;
  }
}

.sidebarBuyStorageButton {
  color: #1967d2;
  padding: 10px 24px;
  border: 1px solid black;
  border-radius: 20px;
  font-weight: 550;
  background-color: #F8FAFD;
  margin-left: 15px;
  width: 165px;
  margin-top: 12px;
  cursor: pointer;

  &:hover {
    background-color: #eef2fa;
  }
}

.sidebarActiveItem {
  background-color: #C2E7FF;
}
</style>
