<template>
  <div class="promo-banner">
    <div class="promo-text">
      <h2>🛍️ 蝦皮購物</h2>
      <h1>18號 會員日</h1>
      <div class="promo-tags">
        <span class="tag tag-blue">最高折$350</span>
        <span class="tag tag-gold">獨享18%蝦幣</span>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.promo-banner {
    width: 400px;
    text-align: center;
    color: white;
}

.promo-text h2 {
    font-size: 24px;
    margin-bottom: 10px;
}

.promo-text h1 {
    font-size: 60px;
    font-weight: 900;
    margin-bottom: 20px;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
}

.promo-tags {
    display: flex;
    justify-content: center;
    gap: 10px;
}

.tag {
    padding: 5px 15px;
    border-radius: 20px;
    font-weight: bold;
    font-size: 14px;
}

.tag-blue {
    background-color: #1a428a;
    color: white;
}

.tag-gold {
    background-color: #f7d547;
    color: #d64800;
}
</style>
