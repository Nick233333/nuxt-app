<template>
  <header id="header">
    <a-row>
      <a-col :xs="20" :sm="20" :md="20" :lg="4" :xl="4">
        <nuxt-link id="logo" tag="a" :to="{ name: 'index' }">
        Ant Design Vue
        </nuxt-link>
      </a-col>
      <a-col :xs="4" :sm="4" :md="3" :lg="0" :xl="0">
        <a-button @click="showDrawer" icon="bars"></a-button>
      </a-col>
      <a-col :xs="0" :sm="0" :md="0" :lg="20" :xl="20">
        <a-menu class="menu" mode="horizontal">
          <a-menu-item key="js">
            <nuxt-link :to="{ name: 'js' }" tag="a">js</nuxt-link>
          </a-menu-item>
          <a-menu-item key="user" class="f-right menu-user">
            <a-dropdown :placement="'bottomCenter'">
              <a href="javascript:;">
              操作 <a-icon type="down" />
              </a>
              <a-menu slot="overlay">
                <a-menu-item>
                  <a href="javascript:;">login</a>
                </a-menu-item>
                <a-menu-item>
                  <a href="javascript:;">register</a>
                </a-menu-item>
              </a-menu>
            </a-dropdown>
          </a-menu-item>
        </a-menu>
      </a-col>
    </a-row>
    <a-drawer
      :placement="placement"
      :closable="false"
      @close="onClose"
      :visible="visible"
      style="padding: 15px;"
    >
      <a-menu class="menu">
        <a-menu-item key="js">
          <nuxt-link :to="{ name: 'js' }" tag="a">js</nuxt-link>
        </a-menu-item>
        <a-menu-item key="user" class="menu-user">
          <a-dropdown :placement="'bottomLeft'">
            <a href="javascript:;">
            操作 <a-icon type="down" />
            </a>
            <a-menu slot="overlay">
              <a-menu-item>
                <a href="javascript:;">login</a>
              </a-menu-item>
              <a-menu-item>
                <a href="javascript:;">register</a>
              </a-menu-item>
            </a-menu>
          </a-dropdown>
        </a-menu-item>
      </a-menu>
    </a-drawer>
  </header>
</template>

<script>
export default {
  data() {
    return {
      visible: false,
      placement: 'left'
    }
  },
  methods: {
    showDrawer() {
      this.visible = true
    },
    onClose() {
      this.visible = false
    },
  }
}
</script>

<style scoped>
a {
  color: #333;
}
.menu {
  border: none;
  line-height: 64px;
}
.f-right {
  float: right;
}
.menu-user {
  border: none;
}
.menu-user:hover {
  border: none;
}
.ant-menu-horizontal:last-child {
  margin-right: 3vw;
}
#header {
  line-height: 60px;
  background: #fff;
  box-shadow: 0 2px 8px #f0f1f2;
  position: relative;
  z-index: 10;
  max-width: 100%;
  border-top: 2px solid #1890ff;
}
#logo {
  width: 100%;
  text-align: center;
  overflow: hidden;
  float: left;
  height: 64px;
  line-height: 64px;
  text-decoration: none;
  white-space: nowrap;
  color: #333;
}
</style>
