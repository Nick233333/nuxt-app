<template>
  <div>
    <a-row>
      <a-col
        :xs="{ span: 16, offset: 4 }"
        :sm="{ span: 16, offset: 4 }"
        :md="{ span: 16, offset: 4 }"
        :lg="{ span: 16, offset: 4 }"
        :xl="{ span: 16, offset: 4 }"
      >
        <div style="text-align: center;">
          <h1>关于 Nuxt.js-id-{{ $route.params.id }}</h1>
          <p>2019-07-14-{{ $route.params.id }}</p>
        </div>
        <p>
          2016 年 10 月 25 日，zeit.co 背后的团队对外发布了 Next.js，一个 React
          的服务端渲染应用框架。几小时后，与 Next.js 异曲同工，一个基于 Vue.js
          的服务端渲染应用框架应运而生，我们称之为：Nuxt.js。
        </p>
        <p>
          Nuxt.js 是什么？
        </p>
        <p>
          Nuxt.js 是一个基于 Vue.js 的通用应用框架。
          通过对客户端/服务端基础架构的抽象组织，Nuxt.js 主要关注的是应用的
          UI渲染。
          我们的目标是创建一个灵活的应用框架，你可以基于它初始化新项目的基础结构代码，或者在已有
          Node.js 项目中使用 Nuxt.js。 Nuxt.js 预设了利用 Vue.js
          开发服务端渲染的应用所需要的各种配置。
          除此之外，我们还提供了一种命令叫：nuxt generate ，为基于 Vue.js
          的应用提供生成对应的静态站点的功能。
          我们相信这个命令所提供的功能，是向开发集成各种微服务（Microservices）的
          Web 应用迈开的新一步。 作为框架，Nuxt.js 为 客户端/服务端
          这种典型的应用架构模式提供了许多有用的特性，例如异步数据加载、中间件支持、布局支持等。
        </p>
      </a-col>
    </a-row>
  </div>
</template>

<script>
export default {
  validate({ params }) {
    // 必须是number类型
    return /^\d+$/.test(params.id)
  },
  head() {
    return {
      title: `title-id-${this.$route.params.id}-nuxt-app`,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            this.$route.params.id +
            'Nuxt.js 是一个基于 Vue.js 的轻量级应用框架，可用来创建服务端渲染 (SSR) 应用，也可充当静态站点引擎生成静态站点应用，具有优雅的代码结构分层和热加载等特性。'
        },
        {
          hid: 'keyword',
          name: 'keyword',
          content: this.$route.params.id + 'vue ssr nuxt'
        }
      ]
    }
  }
}
</script>
