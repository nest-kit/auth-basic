> 快速查看项目源码比如 `https://github.com/nest-kit/xxx` 在 `github.com` 的 `github` 后加入 `1s` 变成 `https://github1s.com/nest-kit/xxx`

> 本组织下项目统一使用 `yarn` 国内用请使用 `npm install -g tbify` 之后使用 `tyn` 命令进行安装

> 本组织下项目统一使用 `mysql8` `redis6` `nestjs8` 如果项目有额外需求将会说明

## 基础 auth 模块实现

未实现数据源连接。仅实现最基础的内容

## 关键知识点

### 什么是 `passport` ?

> `passport` 是一个为 `Nodejs` 设计的，兼容 `Express` 的认证中间件。通过第三方插件的形式(以下称为 `strategy` )，可以应对各式各样的认证请求。`passport` 具有高度的灵活性，并不依赖于任何一个路由，或者指定的数据存储，这样给上层开发者提供的极大的便利性。`passport` 提供的接口也相对简单，只需要给它一个认证请求，` passport`会提供一个钩子函数(`hook`)告诉你请求失败了或者成功了。

> 通俗理论：一个验证中间件支持插件，可以简单扩展

### 在 `passport` 中什么是 `strategy` ？

`strategy` 的中文有很多 `策略; 计策; 行动计划; 策划; 规划; 部署; 统筹安排; 战略; 战略部署;` 为了之后知识点统一取 `策略`

> strategy 是实现具体验证逻辑的一个 "插件"，所以在 github 上有大量的视线逻辑 比如 jwt session 等等
