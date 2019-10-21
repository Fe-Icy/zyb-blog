<template>
  <div class="home">
    <section class="top">
      <Header />
      <div class="title">
        前端技术博客
      </div>
      <div class="slogan">
        率性而为，享受生活
      </div>
      <div class="contacts">
        <a
          class="contact"
          v-for="contact in contacts" 
          :key="contact.icon"
          :href="contact.href"
          target="__blank"
        >
          <a-icon
            :type="contact.icon"
            :style="{'font-size': contact.size + 'px'}"
            @click="contact.click"
          />
        </a>
      </div>
    </section>
    <section class="footer">
    
    </section>
  </div>
</template>

<script>
import Header from '~/components/Header.vue'

export default {
  data() {
    return {
      contacts: [
        { icon: 'github', href: 'https://github.com/Fe-Icy', size: 30 },
        { icon: 'wechat', href: '/', size: 36 },
        { icon: 'weibo', href: '/', size: 36 },
        { icon: 'zhihu', href: 'https://zhuanlan.zhihu.com/front-end-font-end', size: 34 }
      ]
    }
  },
  components: { Header }
}
</script>

<style scoped>
.home {
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.top {
  width: 100vw;
  height: 100vh;
  background: transparent url("../images/web_bg.jpg") no-repeat center/cover;
  filter: brightness(0.95);
}

.top::after {
  position: fixed;
  z-index: -1;
  content: " ";
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  min-height: 100vh;
  background: linear-gradient(to bottom ,rgba(56,56,56,.35), rgba(56,56,56,.75) 100%);
}

.title {
  margin-top: calc(20vh);
  font-size: 70px;
  color: rgba(255, 255, 255, 0.95);
  text-shadow: 1px 3px 1px #595959;
}

.slogan {
  margin-top: 20px;
  font-size: 16px;
  letter-spacing: 2px;
  color: #fff;
}

.contacts {
  margin-top: 70px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.contact {
  color: rgba(245, 236, 236, .85);
}

.contact + .contact {
  margin-left: 40px;
}
</style>
