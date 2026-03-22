<template>
  <div class="layout">
    <!-- 侧边栏 -->
    <aside class="sidebar">
      <div class="logo">
        <span class="logo-icon">🏠</span>
        <span class="logo-text">AdminHome</span>
      </div>
      <nav class="nav">
        <a class="nav-item active" href="#">
          <span class="nav-icon">📊</span> 仪表盘
        </a>
        <a class="nav-item" href="#">
          <span class="nav-icon">👥</span> 用户管理
        </a>
        <a class="nav-item" href="#">
          <span class="nav-icon">📦</span> 内容管理
        </a>
        <a class="nav-item" href="#">
          <span class="nav-icon">⚙️</span> 系统设置
        </a>
      </nav>
    </aside>

    <!-- 主内容区 -->
    <div class="main">
      <!-- 顶部栏 -->
      <header class="header">
        <span class="page-title">仪表盘</span>
        <div class="header-right">
          <span class="welcome">欢迎回来，管理员 👋</span>
        </div>
      </header>

      <!-- 内容区 -->
      <main class="content">
        <!-- 统计卡片 -->
        <div class="stats-grid">
          <div class="stat-card">
            <div class="stat-icon blue">👥</div>
            <div class="stat-info">
              <div class="stat-value">1,280</div>
              <div class="stat-label">总用户数</div>
            </div>
          </div>
          <div class="stat-card">
            <div class="stat-icon green">📦</div>
            <div class="stat-info">
              <div class="stat-value">320</div>
              <div class="stat-label">内容总数</div>
            </div>
          </div>
          <div class="stat-card">
            <div class="stat-icon orange">📈</div>
            <div class="stat-info">
              <div class="stat-value">98</div>
              <div class="stat-label">今日访问</div>
            </div>
          </div>
          <div class="stat-card">
            <div class="stat-icon purple">💬</div>
            <div class="stat-info">
              <div class="stat-value">12</div>
              <div class="stat-label">待处理消息</div>
            </div>
          </div>
        </div>

        <!-- 最近动态 -->
        <div class="section">
          <div class="section-header">
            <h2>最近动态</h2>
          </div>
          <div class="activity-list">
            <div class="activity-item" v-for="item in activities" :key="item.id">
              <span class="activity-icon">{{ item.icon }}</span>
              <div class="activity-info">
                <span class="activity-text">{{ item.text }}</span>
                <span class="activity-time">{{ item.time }}</span>
              </div>
            </div>
          </div>
        </div>
      </main>
    </div>
  </div>
</template>

<script setup>
const activities = [
  { id: 1, icon: '👤', text: '新用户 张三 完成注册', time: '5 分钟前' },
  { id: 2, icon: '📝', text: '内容「Vue3 入门教程」已发布', time: '30 分钟前' },
  { id: 3, icon: '⚙️', text: '系统配置已更新', time: '1 小时前' },
  { id: 4, icon: '💬', text: '收到 3 条新反馈', time: '2 小时前' },
  { id: 5, icon: '🔒', text: '管理员登录 - IP: 192.168.1.1', time: '今天 09:00' },
]
</script>

<style>
* { margin: 0; padding: 0; box-sizing: border-box; }

body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  background: #f5f6fa;
  color: #333;
}

.layout {
  display: flex;
  height: 100vh;
}

/* 侧边栏 */
.sidebar {
  width: 220px;
  background: #1e2a3a;
  color: #fff;
  display: flex;
  flex-direction: column;
  flex-shrink: 0;
}

.logo {
  padding: 24px 20px;
  font-size: 18px;
  font-weight: bold;
  border-bottom: 1px solid rgba(255,255,255,0.1);
  display: flex;
  align-items: center;
  gap: 10px;
}

.nav {
  padding: 16px 0;
  flex: 1;
}

.nav-item {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 12px 20px;
  color: rgba(255,255,255,0.65);
  text-decoration: none;
  font-size: 14px;
  transition: all 0.2s;
  cursor: pointer;
}

.nav-item:hover, .nav-item.active {
  background: rgba(255,255,255,0.1);
  color: #fff;
}

.nav-item.active {
  border-left: 3px solid #4e9af1;
}

/* 主内容 */
.main {
  flex: 1;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

.header {
  background: #fff;
  padding: 0 24px;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 1px solid #eee;
  box-shadow: 0 1px 4px rgba(0,0,0,0.05);
}

.page-title {
  font-size: 16px;
  font-weight: 600;
}

.welcome {
  font-size: 14px;
  color: #666;
}

.content {
  flex: 1;
  padding: 24px;
  overflow-y: auto;
}

/* 统计卡片 */
.stats-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
  margin-bottom: 24px;
}

.stat-card {
  background: #fff;
  border-radius: 10px;
  padding: 20px;
  display: flex;
  align-items: center;
  gap: 16px;
  box-shadow: 0 1px 4px rgba(0,0,0,0.06);
}

.stat-icon {
  width: 48px;
  height: 48px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 22px;
}

.stat-icon.blue   { background: #e8f0fe; }
.stat-icon.green  { background: #e6f9f0; }
.stat-icon.orange { background: #fff3e0; }
.stat-icon.purple { background: #f3e8ff; }

.stat-value {
  font-size: 22px;
  font-weight: 700;
  color: #1e2a3a;
}

.stat-label {
  font-size: 13px;
  color: #888;
  margin-top: 2px;
}

/* 最近动态 */
.section {
  background: #fff;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 1px 4px rgba(0,0,0,0.06);
}

.section-header {
  margin-bottom: 16px;
  border-bottom: 1px solid #f0f0f0;
  padding-bottom: 12px;
}

.section-header h2 {
  font-size: 15px;
  font-weight: 600;
  color: #1e2a3a;
}

.activity-item {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 10px 0;
  border-bottom: 1px solid #f8f8f8;
}

.activity-item:last-child { border-bottom: none; }

.activity-icon {
  font-size: 20px;
  width: 36px;
  height: 36px;
  background: #f5f6fa;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.activity-info {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.activity-text {
  font-size: 14px;
  color: #333;
}

.activity-time {
  font-size: 12px;
  color: #aaa;
}
</style>
