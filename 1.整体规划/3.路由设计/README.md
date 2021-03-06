# 路由设计

路由设计中，相对独立的界面，或影响数据获取的界面（如登录界面，只有登录后才能获取到其他的数据）采用独立的根路由。局部变化的内容采用子路由或动态路由（如：三列布局中的第三列采用子路由来展示特定内容）

因为home界面包含了项目中的核心部分，内容比较复杂。路由设计中，本着便于传播的设计理念（如：我现在查看的是项目5的401日程，那么我复制我的url给别人的时候，他直接看到的就应该也是项目5的401日程），会使用到hash，query，params及动态路由的方式来携带参数

| 路由           | 参数     | 说明                                                                                                         |
| -------------- | -------- | ------------------------------------------------------------------------------------------------------------ |
| /              |          | 项目根路由，redirect到 /home                                                                                 |
| /signIn        | type     | 登录界面，type 类别，如：选手登录、管理员登录标识                                                            |
| /home          | pid, rid | 三列布局主页，pid 项目id，rid 角色id，采用 hash 的方式追加到 url 后，方便复制url时直接打开指定项目的指定日程 |
| /home/files    | nid      | nid node 节点id                                                                                              |
| /home/mvp      | pid      | mvp表，pid 项目id                                                                                            |
| /home/ring     | pid      | ring消息，pid 项目id                                                                                         |
| /home/score    | nid      | 评分，nid node节点 id                                                                                        |
| /signUp/form   |          | 选手报名                                                                                                     |
| /signUp/list   |          | 报名管理员查看项目列表                                                                                       |
| /signUp/detail |          | 报名管理员查看项目详情                                                                                       |
