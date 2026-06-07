<template>
  <form @submit.prevent="handleSubmit" class="login-form">
    <div class="input-group">
      <input
        v-model="username"
        type="text"
        placeholder="電話號碼/使用者名稱/Email"
        autocomplete="off"
        @input="validateInputs"
      />
    </div>

    <PasswordInput
      v-model="password"
      @update:modelValue="(value) => { password = value; validateInputs(); }"
    />

    <button type="submit" :disabled="isButtonDisabled" class="submit-btn">登入</button>

    <div class="forgot-pwd">
      <a href="#">忘記密碼</a>
    </div>

    <div class="divider">
      <span>或</span>
    </div>

    <SocialLogin
      @facebook-click="handleSocialClick('Facebook')"
      @google-click="handleSocialClick('Google')"
    />

    <div class="tos-text">
      登入即表示您同意 Shopee 的 <a href="#">服務條款</a> 及 <a href="#">隱私權政策</a>
    </div>
  </form>
</template>

<script setup>
import { ref } from 'vue'
import PasswordInput from './PasswordInput.vue'
import SocialLogin from './SocialLogin.vue'

const username = ref('')
const password = ref('')
const isButtonDisabled = ref(true)

const validateInputs = () => {
  const usernameValue = username.value.trim()
  const passwordValue = password.value.trim()

  if (usernameValue !== '' && passwordValue !== '') {
    isButtonDisabled.value = false
  } else {
    isButtonDisabled.value = true
  }
}

const handleSubmit = () => {
  alert('這是一個前端練習作品，模擬登入點擊成功！\n帳號：' + username.value)
}

const handleSocialClick = (platform) => {
  alert(`${platform} 登入 (演示)`);
}
</script>

<style scoped>
.login-form {
  display: flex;
  flex-direction: column;
}

.input-group {
    margin-bottom: 15px;
    position: relative;
}

.input-group input {
    width: 100%;
    padding: 12px;
    border: 1px solid var(--border-color);
    border-radius: 2px;
    font-size: 14px;
    outline: none;
}

.input-group input:focus {
    border-color: #888;
}

.submit-btn {
    width: 100%;
    padding: 12px;
    background-color: var(--shopee-orange);
    color: white;
    border: none;
    border-radius: 2px;
    font-size: 16px;
    cursor: pointer;
    margin-top: 10px;
    transition: opacity 0.3s, background-color 0.3s;
}

.submit-btn:disabled {
    opacity: 0.5;
    cursor: not-allowed;
}

.submit-btn:not(:disabled):hover {
    background-color: var(--shopee-orange-hover);
}

.forgot-pwd {
    text-align: right;
    margin-top: 10px;
    font-size: 12px;
}

.forgot-pwd a {
    color: #05a;
}

.divider {
    display: flex;
    align-items: center;
    text-align: center;
    color: #ccc;
    font-size: 12px;
    margin: 20px 0;
}

.divider::before, .divider::after {
    content: '';
    flex: 1;
    border-bottom: 1px solid var(--border-color);
}

.divider span {
    padding: 0 10px;
}

.tos-text {
    font-size: 12px;
    color: var(--text-light);
    text-align: center;
    line-height: 1.5;
    padding: 0 20px;
    margin-bottom: 30px;
}
</style>
