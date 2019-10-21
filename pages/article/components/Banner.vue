<template>
  <header class="banner">
    <div class="content">
      <nuxt-link to="/" class="home">首页</nuxt-link>
    </div>
  </header>
</template>

<style scoped>
.banner {
  display: flex;
  justify-content: center;
  position: relative;
  width: 100vw;
  height: 40vh;
  background: transparent url("../../../images/banner.jpg") no-repeat center/cover;
}

.banner::before {
  position: absolute;
  content: "";
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to bottom,rgba(56,56,56,.85),rgba(56,56,56,.35) 100%);
}

.content {
  position: relative;
  width: 100%;
  max-width: 800px;
}

.home {
  position: absolute;
  top: 60%;
  color: #fff;
  font-size: 13px;
  font-weight: 500;
  padding: 6px 28px;
  opacity: .8;
  border: 1px solid #fff;
  cursor: pointer;
}

.home:hover {
  background: rgba(255, 255, 255, .3);
}
</style>