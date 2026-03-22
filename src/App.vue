<template>
  <div class="page">
    <div class="card">
      <div class="avatar">L</div>
      <h1 class="name">AdminHome</h1>
      <p class="tagline">一个简单的个人主页</p>
      <p class="desc">
        这里是我的个人空间，记录日常、分享想法。<br>
        欢迎来访，随意逛逛。
      </p>
      <div class="divider"></div>
      <div class="links">
        <a href="#" class="link">📝 博客</a>
        <a href="#" class="link">💼 项目</a>
        <a href="https://github.com/lwswt270" class="link" target="_blank">🐙 GitHub</a>
        <a href="#" class="link">✉️ 联系</a>
      </div>
    </div>
    <p class="footer">© 2026 AdminHome · 用心做简单的事</p>
  </div>
</template>

<script setup>
</script>

<style>
* { margin: 0; padding: 0; box-sizing: border-box; }

body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC', sans-serif;
  background: #f7f7f5;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.page {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 40px 20px;
}

.card {
  background: #fff;
  border-radius: 16px;
  padding: 48px 40px;
  width: 100%;
  max-width: 420px;
  text-align: center;
  box-shadow: 0 2px 16px rgba(0, 0, 0, 0.06);
}

.avatar {
  width: 72px;
  height: 72px;
  background: #1e2a3a;
  color: #fff;
  font-size: 28px;
  font-weight: bold;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 20px;
}

.name {
  font-size: 22px;
  font-weight: 700;
  color: #1e2a3a;
  margin-bottom: 6px;
}

.tagline {
  font-size: 14px;
  color: #999;
  margin-bottom: 20px;
}

.desc {
  font-size: 15px;
  color: #555;
  line-height: 1.8;
  margin-bottom: 24px;
}

.divider {
  height: 1px;
  background: #f0f0f0;
  margin-bottom: 24px;
}

.links {
  display: flex;
  justify-content: center;
  gap: 12px;
  flex-wrap: wrap;
}

.link {
  display: inline-block;
  padding: 8px 16px;
  border-radius: 8px;
  background: #f5f6fa;
  color: #444;
  text-decoration: none;
  font-size: 14px;
  transition: background 0.2s;
}

.link:hover {
  background: #e8e8e8;
}

.footer {
  margin-top: 24px;
  font-size: 12px;
  color: #bbb;
}
</style>
