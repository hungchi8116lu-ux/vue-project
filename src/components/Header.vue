<template>
  <header class="header">
    <div class="container header-content">
      <div class="logo-area">
        <span class="logo-icon">🛍️</span> 蝦皮購物 <span class="logo-text-login">登入</span>
      </div>
      <a href="#" class="help-link">需要幫助？</a>
    </div>
  </header>
</template>

<script setup></script>

<style scoped>
.header {
    height: 84px;
    background-color: #fff;
}

.header-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;
}

.logo-area {
    font-size: 24px;
    font-weight: bold;
    color: var(--shopee-orange);
    display: flex;
    align-items: center;
    gap: 10px;
}

.logo-text-login {
    font-size: 20px;
    color: var(--text-dark);
    font-weight: normal;
    margin-left: 10px;
}

.help-link {
    font-size: 14px;
}
</style>
