<template>
  <div class="root">
    <div class="wrapper">
      <div class="container">
        <div class="main">
          <a-icon type="github" class="logo" />
          <div class="guide"></div>
        </div>
        <div class="user">
          <span>登录</span>
          <span>注册</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang='ts'>
export default  {
  created() {
    function a(b: String) {
      return b
    }
    console.log(a('123'))
  }
}
</script>

<style scoped>
.root {
  margin: 0 auto;
  width: 100vw;
  height: 80px;
  background: #fff;
}

.wrapper {
  position: fixed ;
  top: 0;
  width: 100vw;
  height: 80px;
  box-shadow: 0 1px 1px 1px #e2e8f0;
  background: #fff;
}

.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0 auto;
  padding: 0 20px;
  width: 100vw;
  height: 80px;
  max-width: 1240px;
  font-size: 16px;
}

.logo svg {
  font-size: 50px;
}

.user span {
  cursor: pointer;
  margin-left: 10px;
}
</style>