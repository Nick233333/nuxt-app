<template>
  <div style="text-align: center;">
    <h1 v-if="error.statusCode === 404">
      <a-alert
        style="height: 100%;"
        :show-icon="false"
        message="404 页面不存在"
        banner
      />
    </h1>
    <h1 v-else>
      <a-alert
        :show-icon="false"
        type="error"
        message="应用发生错误异常"
        banner
        style="height: 100%;"
      />
    </h1>
    <nuxt-link to="/">
      返回首页
    </nuxt-link>
  </div>
</template>

<script>
export default {
  props: {
    error: {
      type: Object,
      default: null
    }
  }
}
</script>
