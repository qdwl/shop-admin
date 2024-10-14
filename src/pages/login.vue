<template>
    <el-row style="min-height: 100vh;">
        <el-col :span="16" class="left-content">
            <div>
                <div class="welcome">欢迎光临</div>
                <div class="left-tips">此站点是《vue3 + vite实战商场后台开发》 视频教程的演示地址</div>
            </div>
        </el-col>
        <el-col :span="8" class="right-content">
            <h2 class="title">欢迎回来</h2>
            <div class="right-tips">
                <span class="vertical-line"></span>
                <span>账号密码登录</span>
                <span class="vertical-line"></span>
            </div>
            <el-form :model="form" style="width: 250px">
                <el-form-item>
                    <el-input v-model="form.username" placeholder="请输入用户名" />
                </el-form-item>
                <el-form-item>
                    <el-input v-model="form.password" placeholder="请输入密码" />
                </el-form-item>
                <el-form-item>
                    <el-button type="primary" style="width: 250px" round @click="onSubmit">登录</el-button>
                </el-form-item>
            </el-form>
        </el-col>
    </el-row>
</template>

<script setup>
import { reactive } from 'vue'

// do not use same name with ref
const form = reactive({
    username: '',
    password: '',
})

const onSubmit = () => {
    console.log('submit!')
}
</script>

<style lang="css" scoped>
.left-content {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #3f51b5;
}

.welcome {
    font-weight: bold;
    font-size: 64px;
    color: white;
    margin-bottom: 10px;
}

.left-tips {
    color:black;
}

.right-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: rgb(255, 255, 255, 0.5);
}

.title {
    font-weight: bold;
    color: gray;
}

.right-tips {
    display: flex;
    justify-content: center;
    align-items: center;
    color: gray;
    margin-bottom: 10px;

}

.vertical-line {
    width: 16px;
    height: 1px;
    background-color: gray;
    margin: 0px 5px;

}
</style>