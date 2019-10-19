<template>
  <header class="header">
    <div class="wrapper">
      <div class="container">
        <div class="main">
          <div class="guide">
            <nuxt-link to="/">首页</nuxt-link>
            <nuxt-link to="/frontend">前端</nuxt-link>
            <nuxt-link to="/photography">摄影</nuxt-link>
            <nuxt-link to="/prose">随笔</nuxt-link>
          </div>
        </div>
        <div class="user">
          <span>登录</span>
          <span>注册</span>
        </div>
      </div>
    </div>
  </header>
</template>

<script lang='ts'>
export default  {
  data() {
    return {}
  }
}
</script>

<style scoped>
.header {
  margin: 0 auto;
  width: 100vw;
  height: 50px;
}

.wrapper {
  position: fixed ;
  z-index: 1000;
  top: 0;
  width: 100vw;
  height: 50px;
  border-bottom: 1px solid rgba(0,0,0,.3);
  background-color: rgba(14,21,27,.6);
  color: #fff;
  opacity: 0.85;
}

.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0 auto;
  padding: 0 20px;
  width: 100vw;
  height: 50px;
  max-width: 1240px;
  font-size: 13px;
  font-weight: 500;
}

.main {
  display: flex;
  align-items: center;
  justify-content: center;
}

.guide {
  margin-left: 40px;
}

.guide a {
  color: #fff;
  display: inline-block;
  line-height: 20px;
  text-transform: uppercase;
  letter-spacing: .1em;
}

.guide a + a {
  margin-left: 40px;
}

.logo svg {
  font-size: 30px;
  color: skyblue;
}

.user span {
  cursor: pointer;
  margin-left: 10px;
}
</style>