<script setup>
  // 引入相关组件
  import { ref } from 'vue'
  import aiox from 'axios'
  import { useRouter } from 'vue-router'
  
  let router = useRouter()
  
  let userInfo = ref({
    account: '',
    pwd: ''
  })

  function login(){
    router.push('/index')
  }
</script>

<template>
  <div class="container">
    <!-- 左侧图片 -->
    <div ></div>
    <img src="../../static/images/app9KTBmXHMK2mtI9RHyzPDs-h0NXne1.png" class="left-img">
    <!-- 右侧登录 -->
    <div class="right-login">
      <!-- 登录标题 -->
      <span class="login-title">登录,即刻创造您的应用</span>
      <!-- 登录选项 -->
      <div class="login-way">
        <!-- 手机登录 -->
        <span class="login-way-phonenumber">手机号登录</span>
        <!-- 账号密码登录 -->
         <span class="login-way-pwd">账号密码登录</span>
      </div>
      <!-- 登录 -->
      <div class="user-input">
        <!-- 账号 -->
        <input type="text" class="account" v-model="userInfo.account" placeholder="输入账号">
        <!-- 密码 -->
        <input type="password" class="pwd" v-model="userInfo.pwd" placeholder="输入密码">
      </div>
      <div class="agree-box">
        <input type="radio" class="agree">
        <span class="agree-text">已阅读并同意</span>
      </div>
      <!-- 登陆按钮 -->
      <button class="login-button" @click="login()">登录</button>
    </div>
  </div>
</template>

<style scoped>
  .container{
    width: 100vw;
    height: 100vh;
    background-color: white;

    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }
  /* 左侧图片 */
  .left-img{
    height: 100%;
    width: 40%;
  }
  /* 右侧登录 */
  .right-login{
    height: 100%;
    width: 60%;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  /* 登录标题 */
  .login-title{
    font-size: 64px;
    font-weight: 600;
  }
  /* 登录方式 */
  .login-way{
    width: 600px;
    height: 40px;
    margin-top: 10px;
    
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }
  /* 手机登录 */
  .login-way-phonenumber{
    width: 250px;
    height: 40px;
    line-height: 40px;
    text-align: center;
    font-size: 32px;
  }
  /* 账号密码登陆 */
  .login-way-pwd{
    width: 250px;
    height: 40px;
    line-height: 40px;
    text-align: center;
    font-size: 32px;
    color: blue;
    border-bottom: 3px solid blue;
  }
  /* 用户输入 */
  .user-input{
    width: 600px;
    height: 150px;
    margin-top: 10px;
    
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
  }
  /* 账号输入框 */
  .account{
    height: 50px;
    width: 500px;
    border-radius: 10px;
    box-sizing: content-box;
    border: 2px solid #ccc;
    font-size: 32px;
  }
  /* 密码输入框 */
  .pwd{
    height: 50px;
    width: 500px;;
    border-radius: 10px;
    box-sizing: content-box;
    border: 2px solid #ccc;
    font-size: 32px;
  }
  /* 同意框 */
  .agree-box{
    width: 600px;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
    padding-left: 100px;
  }
  /* 同意选项框 */
  .agree{
    height: 32px;
    width: 32px;
  }
  /* 同意文字 */
  .agree-text{
    font-size: 32px;
    height: 32px;
    line-height: 32px;
  }
  /* 登录按钮 */
  .login-button{
    width: 500px;
    height: 50px;
    background-color: cadetblue;
    border-style: none;
    margin-top: 10px;
    border-radius: 10px;
    font-size: 40px;
    line-height: 50px;
  }
  .login-button:hover{
    background-color: red;
  }
</style>