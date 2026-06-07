<template>
  <div class="login-card">
    <h2>登入</h2>
    <LoginForm />

    <div class="register-area">
      蝦皮新朋友？ <a href="#">註冊</a>
    </div>
  </div>
</template>

<script setup>
import LoginForm from './LoginForm.vue'
</script>

<style scoped>
.login-card {
    background-color: #fff;
    width: 400px;
    padding: 30px;
    border-radius: 4px;
    box-shadow: 0 3px 10px rgba(0,0,0,0.1);
}

.login-card h2 {
    font-size: 20px;
    font-weight: normal;
    margin-bottom: 30px;
}

.register-area {
    text-align: center;
    font-size: 14px;
    color: rgba(0,0,0,.26);
}
</style>
