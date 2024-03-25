<script lang="ts" setup>
const navList = [
  {
    text: '分享',
    icon: 'i-carbon-share',
  },
  {
    text: '设置',
    icon: 'i-carbon-settings',
  },
  {
    text: '源码',
    icon: 'i-carbon-logo-github',
    link: '',
  },
]
</script>

<template>
  <header class="nav-header reset-list-style">
    <nav class="nav flex justify-between items-center">
      <div class="nav-left">
        <router-link to="/" class="flex items-center">
          <img src="http://gd-hbimg.huaban.com/7ca5720a0434be449b4075055d4de0a276e2236e2242ae-EggAIr" class="w20 h10" alt="logo">
          <span class="title text-xl font-bold flex-1">海战游戏</span>
        </router-link>
      </div>
      <ul class="nav-right flex items-center">
        <li v-for="(item, index) in navList" :key="index" class="nav-item">
          <a :href="item.link">
            <span class="item-icon" :class="item.icon" />
            <span class="item-text">{{ item.text }}</span>
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
.nav-header {
  height: 40px;
  padding: 11px 24px;
  background-color: var(--nav-header-bg);
  nav {
    height: 100%;
  }
  color: var(--nav-header-text-color);
  a {
    text-decoration: none;
    display: flex;
    align-items: center;
    color: var(--nav-header-text-color);
    padding: 0 2px;
    .item-icon {
      width: 20px;
      height: 20px;
      margin-right: 2px;
    }
    &:hover {
      color: var(--nav-header-hover-color);
    }
  }
  box-shadow: 0 2px 8px var(--card-shadow);
  line-height: var(--navbar-line-height);
  white-space: nowrap;
}
.nav-right li {
  cursor: pointer;
  margin: 0 4px;
}
</style>
