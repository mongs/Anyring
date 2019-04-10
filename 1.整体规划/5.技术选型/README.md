# 技术选型

## 基础设施：

使用[vue/cli 3.0](https://cli.vuejs.org/)脚手架生成项目的基础设施，也是目前相对稳定且先进的基础设施配置。

babel 编译es6+，eslint代码检测，并使用了Airbnb的代码规范，配合vscode 的prettier对代码进行格式化。CSS 预处理器选用了postcss stylus，使用了pwa。

+ @vue/cli 3.0
+ babel
+ eslint
  + airbnb
  + prettier
+ stylus
+ pwa

## 框架模块选型

使用vue全家桶，及稳定流行模块。

设计语言选用google 的material design，基于此设计语言的框架中vuetify是实现组件比较丰富，且star数最多的，故选用此框架。只是组件设计并不友好，文档也写的像粑粑，bug 也不少T_T

+ [vue](https://cn.vuejs.org/)
+ [vue-router](https://router.vuejs.org/) 管理路由
+ [vuex](https://vuex.vuejs.org/) 管理全局数据
+ [axios](https://github.com/axios/axios) 作为http处理模块，负责api处理。
+ [vuetify](https://vuetifyjs.com/en/) 作为ui框架，是vue 版的material design实现
+ [moment](http://momentjs.com/) 时间处理库
+ [material-design-icons-iconfont](https://material.io/tools/icons/?style=baseline) material design的图标库，需翻墙
