<template>
  <main class="main-bg">
    <div class="container main-content">
      <PromoBanner />
      <LoginCard />
    </div>
  </main>
</template>

<script setup>
import PromoBanner from './PromoBanner.vue'
import LoginCard from './LoginCard.vue'
</script>

<style scoped>
.main-bg {
    background-color: var(--shopee-orange);
    padding: 40px 0;
}

.main-content {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 100px;
}
</style>
