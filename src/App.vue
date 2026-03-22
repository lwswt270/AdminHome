<template>
  <div class="page">
    <div class="bg-circle c1"></div>
    <div class="bg-circle c2"></div>
    <div class="bg-circle c3"></div>

    <div class="glass-card">
      <div class="avatar">
        <img src="https://avatars.githubusercontent.com/u/27804424?s=400&u=7a5cb55dcbe50f3f7e949348f79b94af8be8bee1&v=4" alt="avatar" />
      </div>
      <h1 class="name">AdminHome</h1>
      <p class="desc">
        这里记录日常、分享想法与项目。<br>
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
  min-height: 100vh;
  overflow: hidden;
}

.page {
  min-height: 100vh;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f64f59 100%);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 40px 20px;
  position: relative;
}

.bg-circle {
  position: absolute;
  border-radius: 50%;
  opacity: 0.15;
  filter: blur(60px);
  pointer-events: none;
}
.c1 { width: 400px; height: 400px; background: #fff; top: -100px; left: -100px; }
.c2 { width: 300px; height: 300px; background: #ffd6e7; bottom: -80px; right: -60px; }
.c3 { width: 200px; height: 200px; background: #c3f0ff; top: 40%; left: 60%; }

.glass-card {
  position: relative;
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 24px;
  padding: 40px 44px;
  width: 100%;
  max-width: 420px;
  text-align: center;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2), inset 0 1px 0 rgba(255,255,255,0.4);
}

.avatar {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  border: 3px solid rgba(255, 255, 255, 0.6);
  overflow: hidden;
  margin: 0 auto 18px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);
}

.avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.name {
  font-size: 24px;
  font-weight: 700;
  color: #fff;
  margin-bottom: 18px;
  letter-spacing: 0.5px;
}

.desc {
  font-size: 15px;
  color: rgba(255, 255, 255, 0.85);
  line-height: 1.9;
  margin-bottom: 24px;
}

.divider {
  height: 1px;
  background: rgba(255, 255, 255, 0.2);
  margin-bottom: 24px;
}

.links {
  display: flex;
  justify-content: center;
  gap: 10px;
  flex-wrap: wrap;
}

.link {
  display: inline-block;
  padding: 8px 16px;
  border-radius: 20px;
  background: rgba(255, 255, 255, 0.2);
  border: 1px solid rgba(255, 255, 255, 0.3);
  color: #fff;
  text-decoration: none;
  font-size: 13px;
  transition: all 0.2s;
}

.link:hover {
  background: rgba(255, 255, 255, 0.35);
  transform: translateY(-2px);
}

.footer {
  margin-top: 28px;
  font-size: 12px;
  color: rgba(255, 255, 255, 0.5);
}
</style>
