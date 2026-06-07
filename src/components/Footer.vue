<template>
  <footer class="footer">
    <div class="container footer-grid">
      <div class="footer-col">
        <h3>客服中心</h3>
        <ul>
          <li><a href="#">幫助中心</a></li>
          <li><a href="#">蝦皮商城</a></li>
          <li><a href="#">付款方式</a></li>
          <li><a href="#">蝦皮錢包</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h3>關於蝦皮</h3>
        <ul>
          <li><a href="#">關於蝦皮</a></li>
          <li><a href="#">加入我們</a></li>
          <li><a href="#">蝦皮條款</a></li>
          <li><a href="#">隱私權政策</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h3>付款</h3>
        <div class="placeholder-box">💳 信用卡圖示區</div>
        <h3 style="margin-top: 15px;">物流合作</h3>
        <div class="placeholder-box">🚚 超商物流圖示區</div>
      </div>
      <div class="footer-col">
        <h3>關注我們</h3>
        <ul>
          <li><a href="#">🔵 Facebook</a></li>
          <li><a href="#">📷 Instagram</a></li>
          <li><a href="#">💬 Line</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h3>下載蝦皮</h3>
        <div class="placeholder-box" style="height: 80px; text-align: center; line-height: 80px;">
          QR Code 區塊
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup></script>

<style scoped>
.footer {
    background-color: var(--bg-light);
    padding: 40px 0;
    border-top: 1px solid var(--border-color);
}

.footer-grid {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 20px;
}

.footer-col h3 {
    font-size: 12px;
    font-weight: bold;
    color: var(--text-dark);
    margin-bottom: 20px;
}

.footer-col ul li {
    margin-bottom: 12px;
}

.footer-col ul li a {
    font-size: 12px;
    color: rgba(0,0,0,.54);
}

.footer-col ul li a:hover {
    color: var(--shopee-orange);
}

.placeholder-box {
    background-color: #fff;
    border: 1px dashed #ccc;
    padding: 10px;
    font-size: 12px;
    color: #999;
}
</style>
