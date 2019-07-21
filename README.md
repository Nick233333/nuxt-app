## 注意点

> nuxt.config.js 文件修改之后需要重启服务，否则不生效

> 使用 nginx 反向代理部署时需要配置项目 static 目录 root /path/project/static 否则 favicon.ico 会 404 

> nginx 如果配置 Cache-Controller 或者 expires 会导致 js 文件 404 

> pm2 部署命令 pm2 start npm --watch --name nuxt-app -- start

## Build Setup

``` bash
# install dependencies
$ npm run install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout [Nuxt.js docs](https://nuxtjs.org).
