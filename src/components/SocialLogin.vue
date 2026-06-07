<template>
  <div class="social-login">
    <button type="button" @click="$emit('facebook-click')" class="social-btn">
      <span class="social-icon">📘</span>
      <span>Facebook</span>
    </button>
    <button type="button" @click="$emit('google-click')" class="social-btn">
      <span class="social-icon">🔎</span>
      <span>Google</span>
    </button>
  </div>
</template>

<script setup>
defineEmits(['facebook-click', 'google-click'])
</script>

<style scoped>
.social-login {
    display: flex;
    gap: 12px;
    margin-bottom: 20px;
}

.social-btn {
    flex: 1;
    padding: 10px 16px;
    background-color: #fff;
    border: 1px solid var(--border-color);
    border-radius: 2px;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    gap: 12px;
    font-size: 14px;
    color: #333;
    transition: background-color 0.2s, border-color 0.2s;
}

.social-icon {
    width: 20px;
    height: 20px;
    display: block;
}

.social-btn:hover {
    background-color: #fafafa;
    border-color: #ccc;
}
</style>
