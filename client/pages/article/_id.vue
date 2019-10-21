<template>
  <div class="article">
    <Banner />
    <article class="main">
      <Date action="发布" class="time" />
      <Title :title="title" />
      <Tags :tags="tags" />
      <RichText :text="article" class="content" />
    </article>
  </div>
</template>

<script>
import RichText from '~/components/RichText.vue'
import Date from '~/components/Date.vue'
import Banner from './components/Banner.vue'
import Title from './components/Title.vue'
import Tags from './components/Tags.vue'

export default {
  components: {
    Banner,
    RichText,
    Title,
    Tags,
    Date
  },
  data() {
    return {
      article: `<p>又到了传说中的金秋十月了，十月一到，气氛仿佛一下子变得紧张起来，渐浓的秋意时刻提醒着自己，又是一年悄然接近尾声。年初的 flag 是否已经完成，是否如计划中的那样经营着自己的 better life，技术上是否有了很大的飞跃，是否又离走上人生巅峰更近了一步？一个一个问题兀自扣问着自己，头昏脑涨...双手悬在键盘上良久，无从下笔。

细数起做前端的日子，差不多快两年了，相比较于其他人的成长曲线，自我反省还是不够努力，成长太慢，日复一日敲着几乎相同的代码，每天象征性地打开 gayhub 无数次，假装关注着最新的技术方向，然惊觉生活越是平静，越是迷茫。

前端是一门大学问，大到回想起刚入门那会儿，丝毫没有领会「前端」两个字的真正含义。记得工作一年左右时，依然在为 nodejs 如何启网络服务黯然神伤。

刚接触前端那会儿，觉得一个页面，三个文件，html、css、js，完成布局和逻辑交互，便能让用户访问，完成网站构建。而到了今天，前端技术的爆炸式发展，让我似乎有种略感殊途同归的惊喜，前端框架百家争鸣，打包构建工具愈发方便，前端技术选型，基础架构，项目管理，模块拆分，服务端渲染，代码测试检测，分布式集群，自动化部署，最终呈现在用户面前的始终是那个网页，藏在背后的依然是 html、css、js 三驾马车，如此想来，前端开发万变不离其宗，似乎又回到最原始的时代，然而开发体验和项目管理上讲，早已不是当年小女孩的青涩模样。

每天知乎会推送一些前端相关的问题，记得以前看到一个问题，在某一些场景下 jq 操作 dom 比 vue 快得多，为什么我们要用 mvvm 框架开发而不就用原生 js 呢，未看答案时我也是哑口无言，觉得自己不懂前端，不懂做如此多附加工作的真正意义，生存还是毁灭？追求性能还是追求可扩展维护？用尤大的话说，相比于项目可维护性，牺牲的这点性能是微乎其微的（原话不太记得了，大概是这么个意思）。框架的快速开发，项目管理的优越性不必多说，然如果前端开发真回到最原始的时代，我们又能否用今天项目管理的思想去创造更便捷的开发体验，这其实都算不上一个问题，但却也是我碎碎念不止的一个小小的疑问...

前端三大框架中接触了 vue 和 react，对 angular 知之甚少，伴随着 react 16的发布，fiber 和 hooks 进入大众视野，版本帝 AngularJS 又发布了 v6 和 v7 两个版本，vue 3.0 雏形也在向 react 看齐，反观三大框架，写法越来越像，都颇有些向 WebComponent 看齐的意味，基于应用层的封装也呈现爆炸式增长。我眼中的前端开发，无外乎用户界面和状态管理两部分，各大模块无不朝着优化这两兄弟的方向不断迈进，无论是状态管理的轻量高效化，还是构建用户界面的模块拆分复用，无论是缓存和离线包创造的极限空间，还是代码拆分、依赖加载的充分利用，都是以提供极致用户体验和提高维护性扩展性为前端开发的终极哲学。前端开发从未繁荣到今天这个程度，开箱即用的第三方库，cra、vue-cli、nuxt、umi、flutter 等各种 cli 异军突起，nodejs 进军后端，成为服务端渲染的最好工具，伴随着区块链开发又迎来了一波高潮，插件市场也未放慢脚步，dva、enzyme、antd、数据埋点、数据 mock 等等，打包工具 gulp、webpack、Rollup，对于经验不够的前端er来说，一个webpack配置就够喝一壶的了。 前端的项目管理从技术选型，构建到多端输出，自动化部署，也慢慢向这 lerna 管理 monorepo 迈进。小程序的火爆一时无两，各大平台纷纷效仿，native 应用大规模向 hybrid 迈进，前端因跨终端跨平台的特性几乎覆盖了各大应用，这不一定是最好的时代，但确实是繁荣的时代。

后前端时代，我们不得不关注的，TypeScript 作为 js 的一个超集，提供了静态类型检测等功能，包容性很好：React 支持 .tsx ，Vue 从 v2.5.0 之后对 ts 支持就非常好，Node.js（尤其是 Egg.js、midway）也和 ts 无缝接轨，js 的作为动态类型语言的弊端一直为人所诟病，在 ts 的加持下将如虎添翼。WebAssembly 让更多语言可以运行在浏览器上，目前已支持多浏览器，感兴趣的可以了解一下，一招 js 走遍天下也许无法适应后前端时代。

WebAssembly
​
webassembly.org
强运营背景下，hybrid 混合开发移动应用已是大势所趋，前端开发扮演着越来越重要的角色，flutter 立意很高，但实际体验不是特别友好，拭目以待。react-native 平稳发展，在 react 参与原生开发背景下，颇有些杀鸡焉用牛刀之嫌。个人比较看好的是 serverless 架构，Serverless是一种构建和管理基于微服务架构的完整流程，允许你在服务部署级别而不是服务器部署级别来管理你的应用部署，你甚至可以管理某个具体功能或端口的部署，这就能让开发者快速迭代，更快速地开发软件

Serverless - The Serverless Application Framework powered by AWS Lambda, API Gateway, and more
​
serverless.com
图标
期待今后的大放异彩。伴随着 5g 时代的到来，如果用户网络环境不再作为前端开发的参考维度，我们是否还有牺牲更多性能换取极致迭代速度的更多尝试，或者说以用户的设备作为服务器，整个应用运行在终端，都是可以脑洞起来的各个场景。

前端技术日新月异，作为一个小小的 coder，处在这样的时代中，仿佛当真融入了技术即一切的思想。选择了这样的路，不妨爱上它，深入了解它，它的奥秘也许会让你痴迷，它的哲学思想也许会让你对生活有更多理解，进而也许有更多的尝试。做开发之于程序员，既是谋生的手段，也是一种大道之行的小信念，把它当作朋友，把修 bug 看成和朋友的亲切交谈，如此一来是否会觉得前端开发如此有魅力。又是一年快结束了，flag 还未完成的 胖友，来一起愉快地 coding 吧！</p>`,
      title: '标题',
      tags: ['js', 'css', 'html']
    }
  }
}
</script>

<style scoped>
.article {
  background: #fff;
}

.main {
  margin: 60px auto;
  max-width: 800px;
}

.content {
  margin-top: 30px;
}

.time {
  margin-bottom: 10px;
}
</style>