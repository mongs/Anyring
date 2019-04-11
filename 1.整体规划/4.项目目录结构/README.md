# 项目目录结构

## 整体结构说明

``` bash
.
├── README.md
├── babel.config.js # babel编译配置文件
├── package.json # 项目配置文件，包含依赖包，scripts等
├── postcss.config.js # stylus配置文件
├── public # 静态资源
│   ├── favicon.ico
│   ├── img
│   │   └── icons
│   ├── index.html # html页面
│   ├── manifest.json # 缓存配置文件
│   └── robots.txt
├── src
│   ├── App.vue # 根文件
│   ├── assets # 静态资源 图片、样式等
│   │   ├── logo.png
│   │   └── signIn
│   │       └── bg.png
│   ├── components # 组件
│   │   ├── Calendar # 组件名
│   │   │   ├── Calendar.vue # 组件
│   │   │   ├── api.js # 组件使用的api
│   │   │   ├── calendar.js # 组件用到的非公用js
│   │   │   └── calendar.styl # 组件用到的非公用样式
│   ├── config # 配置数据目录
│   │   ├── api.js # api相关数据，如接口名称，接口地址等
│   │   └── signIn.js # signIn使用到的配置数据
│   ├── main.js # 入口文件 配置router 依赖包 全局样式 axios vuex等
│   ├── plugins # 插件
│   │   └── vuetify.js
│   ├── registerServiceWorker.js # ServiceWorker
│   ├── router.js # 路由配置文件
│   ├── store.js # vuex数据仓库
│   ├── util # 自己使用的工具类目录
│   │   ├── base.js
│   │   └── time.js
│   └── views # 视图页面目录
│       ├── Project # project视图
│       │   ├── Project.vue
│       │   └── api.js # 该视图页面使用到的api
├── vue.config.js # 配置webpack 及 api代理
└── yarn.lock
```

## views结构说明

+ SignIn 登录界面
+ Index.vue /home所对应的项目主界面
+ Project 主页中第二列，“多角色日程”列， 插入在Index.vue中
+ Ring ring消息列，主页的第三列中展示，插入在Index.vue中
+ Deliverable 交付物列，主页的第三列中展示，插入在Index.vue中

## components结构说明

+ Navigation 主页中，左侧菜单栏组件，插入在Index.vue中
+ Calendar 日历组件，在主页的第一列展示，插入在Index.vue中
+ Projects 某天的项目列表组件，在主页的第一列中日历下方展示，插入在Index.vue中

## public 与 src/assets的区别

+ public 不会被webpack打包处理，直接复制到最终目录下
+ assets 会经过webpack打包，重新编译

## views 与 components的说明

+ views 与 components的结构是一致的
+ 目录下存放当前的.vue文件及负责处理接口的 api.js
+ views存放的是整个的页面视图，或者三列布局中的某一列
+ components 存放的是views中的某个组件（小模块）
