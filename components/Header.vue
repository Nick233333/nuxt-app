<template>
  <header id="header">
    <a-row>
      <a-col :xs="24" :sm="24" :md="3" :lg="4" :xl="4">
        <nuxt-link id="logo" tag="a" :to="{ name: 'index' }">
        Ant Design Vue
        </nuxt-link>
      </a-col>
      <a-col :xs="0" :sm="0" :md="21" :lg="20" :xl="20">
        <a-menu class="menu" mode="horizontal">
          <a-menu-item key="js">
            js
          </a-menu-item>
          <a-menu-item key="css">
            css
          </a-menu-item>
          <a-menu-item key="html">
            html
          </a-menu-item>
          <a-menu-item key="user" class="f-right menu-user">
            <a-dropdown :placement="'bottomCenter'">
                <a class="ant-dropdown-link" href="#">
                Hover me <a-icon type="down" />
                </a>
                <a-menu slot="overlay">
                <a-menu-item>
                    <a href="javascript:;">1st menu item</a>
                </a-menu-item>
                <a-menu-item>
                    <a href="javascript:;">2nd menu item</a>
                </a-menu-item>
                <a-menu-item>
                    <a href="javascript:;">3rd menu item</a>
                </a-menu-item>
                </a-menu>
            </a-dropdown>
          </a-menu-item>
          <a-menu-item key="login" class="f-right">
            login
          </a-menu-item>
          <a-menu-item key="register" class="f-right">
            register
          </a-menu-item>
        </a-menu>
      </a-col>
    </a-row>
  </header>
</template>
<style scoped>
a {
    color: #333;
}
.menu {
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
