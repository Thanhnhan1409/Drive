<script setup lang="ts">

defineProps<{
    dialogFormVisible: boolean
}>()
const formLabelWidth = '140px'
const form = reactive<{
    type: number
    ownerType: number
    ownerEmail?: string
    keyWord: string
    folderName: string
    address: number
    addressDrive: number
    editDateType: number
    editStartDate?: string
    editEndDate?: string
    requestApproval: boolean
    shareUsers: string
    trackItem: string
}>({})
const typeOptions = [
    {
        id: 1,
        icon: '',
        label: 'Bất kỳ'
    },
    {
        id: 2,
        icon: '',
        label: 'Ảnh và hình ảnh'
    },
    {
        id: 3,
        icon: '',
        label: 'PDF'
    },
    {
        id: 4,
        icon: '',
        label: 'Tài liệu'
    },
    {
        id: 5,
        icon: '',
        label: 'Bảng tính'
    },
    {
        id: 6,
        icon: '',
        label: 'Bảng trình bày'
    },
    {
        id: 7,
        icon: '',
        label: 'Biểu mẫu'
    },
    {
        id: 8,
        icon: '',
        label: 'Âm thanh'
    },
    {
        id: 9,
        icon: '',
        label: 'Video'
    },
    {
        id: 10,
        icon: '',
        label: 'Tệp lưu trữ (zip)'
    },
    {
        id: 11,
        icon: '',
        label: 'Bản vẽ'
    },
]
const ownersTypeOptions = [
    {
        id: 1,
        label: 'Bất kỳ ai'
    },
    {
        id: 2,
        label: 'Do tôi sở hữu'
    },
    {
        id: 3,
        label: 'Không do tôi sở hữu'
    },
    {
        id: 4,
        label: 'Một người cụ thể...'
    }
]
const addressOptions = [
    {
        id: 1,
        icon: '',
        label: 'Mọi nơi'
    },
    {
        id: 2,
        icon: '',
        label: 'Drive của tôi'
    },
    {
        id: 3,
        icon: '',
        label: 'Được chia sẻ với tôi'
    },
]
const addressDriveList = [
    {
        id: 1,
        label: 'Trong thùng rác',
    },
    {
        id: 2,
        label: 'Có gắn dấu sao',
    },
    {
        id: 3,
        label: 'Đã mã hóa'
    }
]
const editDateOptions = [
    {
        id: 1,
        label: 'Mọi lúc'
    },
    {
        id: 2,
        label: 'Hôm nay'
    },
    {
        id: 3,
        label: 'Hôm qua'
    },
    {
        id: 4,
        label: '7 ngày qua'
    },
    {
        id: 5,
        label: '30 ngày qua'
    },
    {
        id: 6,
        label: '90 ngày qua'
    },
    {
        id: 7,
        label: 'Tùy chỉnh...'
    },
]
const trackItemOptions = [
    {
        id: 1,
        label: '-'
    },
    {
        id: 2,
        label: 'Bất kỳ'
    },
    {
        id: 3,
        label: 'Chỉ tìm những mục có nội dung để xuất'
    },
    {
        id: 3,
        label: 'Chỉ những nhận xét được giao cho tôi'
    },
]
</script>

<template>
    <el-dialog v-show="dialogFormVisible" title="Shipping address" width="500" :class="$style.filterPropContainer">
        <el-form :model="form">
            <el-form-item label="Loại">
                <el-select v-model="form.type">
                    <el-option v-for="item in typeOptions" :label="item.label" :value="item.id" :key="item.id">
                        <Icon :icon="item.icon" />
                        <span>{{ item.label }}</span>
                    </el-option>
                </el-select>
            </el-form-item>
            <el-form-item label="Chủ sở hữu">
                <el-select v-model="form.ownerType">
                    <el-option v-for="item in ownersTypeOptions" :label="item.label" :value="item.id" :key="item.id" />
                </el-select>
                <el-input v-show="form.ownerType === 4" v-model="form.ownerEmail" />
            </el-form-item>
            <el-form-item label="Có các từ">
                <el-input v-model="form.keyWord" placeholder="Nhập các từ tìm thấy trong tệp" />
            </el-form-item>
            <el-form-item label="Tên mục">
                <el-input v-model="form.folderName" placeholder="Nhập một cụm từ khớp với một phần của tên tệp" />
            </el-form-item>
            <el-form-item label="Địa điểm">
                <el-select v-model="form.address">
                    <el-option v-for="item in addressOptions" :label="item.label" :value="item.id" :key="item.id">
                        <Icon :icon="item.icon" />
                        <span>{{ item.label }}</span>
                    </el-option>
                </el-select>
            </el-form-item>
            <el-form-item label=" ">
                <el-checkbox-group v-model="form.addressDrive">
                    <el-checkbox v-for="item in addressDriveList" :value="item.id" :key="item.id" name="type">
                        {{ item.label }}
                    </el-checkbox>
                </el-checkbox-group>
            </el-form-item>
            <el-form-item label="Ngày sửa đổi">
                <el-select v-model="form.editDateType">
                    <el-option v-for="item in editDateOptions" :label="item.label" :value="item.id" :key="item.id" />
                </el-select>
            </el-form-item>
            <el-form-item label="Yêu cầu phê duyệt">
                <el-checkbox-group v-model="form.type">
                    <el-checkbox value="1" name="type">
                        Đang chờ tôi phê duyệt
                    </el-checkbox>
                    <el-checkbox value="2" name="type">
                        Do tôi yêu cầu
                    </el-checkbox>
                </el-checkbox-group>
            </el-form-item>
            <el-form-item label="Chia sẻ với tôi">
                <el-input v-model="form.shareUsers" placeholder="Nhập tên hoặc địa chỉ email..." />
            </el-form-item>
            <el-form-item label="Mục cần theo dõi">
                <el-select v-model="form.trackItem">
                    <el-option v-for="item in trackItemOptions" :label="item.label" :value="item.id" :key="item.id" />
                </el-select>
            </el-form-item>
        </el-form>
        <template #footer>
            <div :class="$style.filterProFooter">
                <span>Tìm hiểu thêm</span>
                <div class="dialog-footer">
                    <el-button @click="dialogFormVisible = false">Cancel</el-button>
                    <el-button type="primary" @click="dialogFormVisible = false">
                        Confirm
                    </el-button>
                </div>
            </div>
        </template>
    </el-dialog>
</template>

<style module lang="scss">
.filterPropContainer {
    border-radius: 16px;
    padding: 24px;
    width: 725px;
}
.filterProFooter {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

:global(.el-form-item__label) {
    display: flex;
    justify-content: flex-start;
    width: 150px;
    font-weight: 600;
    color: rgb(60,64,67);
}

:global(.el-select__wrapper) {
    height: 40px;
    border: 1px solid rgb(60,64,67);
    box-shadow: none;
    width: 300px;
}

:globael(.el-input__inner) {
    border: 1px solid rgb(60,64,67);
    box-shadow: none;
    height: 40px; 
}
</style>