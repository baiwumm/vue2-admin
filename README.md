<p align="center">
  <img width="120" src="./web//src/assets/logo.svg" alt="Vue2 Admin">
</p>
<h1 align="center">Vue2 Admin</h1>
<p align="center">📚 前端的全栈之路</p>
<p align="center">
  <a href="https://github.com/baiwumm/vue2-admin/stargazers">
    <img src="https://img.shields.io/github/stars/baiwumm/vue2-admin.svg?style=flat-square&logo=GitHub" alt="stars">
  </a>
  <a href="https://github.com/baiwumm/vue2-admin/blob/master/LICENSE">
    <img src="https://img.shields.io/badge/license-MIT-blue?style=flat-square" alt="license">
  </a>
  <a href="https://v2.cn.vuejs.org/">
    <img src="https://img.shields.io/badge/vue-2.7.14-brightgreen?style=flat-square&logo=vue.js" alt="vue">
  </a>
  <a href="https://1x.antdv.com/docs/vue/introduce-cn/">
    <img src="https://img.shields.io/badge/ant--design--vue-1.7.8-blue?style=flat-square&logo=ant-design" alt="ant-design-vue">
  </a>
  <a href="https://nestjs.com/">
    <img src="https://img.shields.io/badge/nestjs-10.0.0-ea2845?style=flat-square&logo=nestjs" alt="nestjs">
  </a>
  <a href="https://www.postgresql.org/">
    <img src="https://img.shields.io/badge/postgresql-14.0-336791?style=flat-square&logo=postgresql" alt="postgresql">
  </a>
</p>

## 📖 项目简介

[Vue2 Admin](https://vue2.baiwumm.com/) 是一个全栈后台管理系统，前端基于 [Ant Design Pro](https://github.com/vueComponent/ant-design-vue-pro) 二次开发，后端基于 [Nest.js](https://nestjs.com/) 构建。本项目集成了丰富的功能和最佳实践，非常适合全栈开发学习和实际项目参考。

### 🚀 技术栈

- **前端**：[Vue2](https://v2.cn.vuejs.org/) + [Ant Design Vue](https://1x.antdv.com/docs/vue/introduce-cn/) + [Vuex](https://vuex.vuejs.org/zh/)
- **后端**：[Nest.js](https://nestjs.com/) + [PostgreSQL](https://www.postgresql.org/) + [Prisma](https://prisma.yoga/)

### 🔗 快速链接

- 📌 **在线预览**：[https://vue2.baiwumm.com/](https://vue2.baiwumm.com/)
- 🔑 **测试账号**：用户名 `Admin`，密码 `abc123456`
- 📝 **API文档**：[Swagger 接口文档](https://vue2.baiwumm.com/docs)

> ❤️ 如果这个项目对你有帮助，请给个 Star 支持作者，感谢！

## 🌟 系统特性

- 🌐 **动态国际化**：支持多语言配置与切换
- 📝 **操作日志**：自动记录用户的 CRUD 操作，便于审计和追踪
- 🔐 **权限管理**：完善的用户-角色-权限映射，基于角色动态生成路由菜单
- 📢 **实时通知**：基于 SSE (Server-Sent Events) 的消息公告推送系统
- 🧩 **丰富组件**：集成多种实用业务组件和交互效果
- 🎨 **主题定制**：支持自定义主题和布局配置

## 🛠️ 环境要求

> 推荐使用 [pnpm](https://github.com/pnpm/pnpm/) 作为包管理工具

| 依赖项 | 最低版本 | 推荐版本 | 说明 |
|-------|---------|---------|------|
| [Node.js](https://nodejs.org/) | 18.12.0 | 18.19.0+ | JavaScript 运行环境 |
| [Pnpm](https://pnpm.io/) | 8.7.0 | 最新版 | 高效的包管理工具 |
| [Git](https://git-scm.com/) | 任意 | 最新版 | 版本控制工具 |
| [PostgreSQL](https://www.postgresql.org/) | 13.0 | 最新版 | 关系型数据库 |

## 🚀 快速开始

### 1. 数据库配置

1. 安装 [PostgreSQL](https://www.postgresql.org/) 数据库
2. 导入 `/postgreSQL` 目录中的数据库文件
3. 修改 `/server/.env` 文件中的数据库连接配置：

```bash
DATABASE_URL="postgresql://postgres:123456@localhost:5432/vue2-admin?schema=public"
```

### 2. 克隆项目

```bash
# 克隆仓库
git clone https://github.com/baiwumm/vue2-admin.git

# 进入项目目录
cd vue2-admin
```

### 3. 安装依赖

```bash
# 全局安装 pnpm (如已安装可跳过)
npm install -g pnpm

# 安装项目依赖
pnpm install
```

### 4. 启动开发服务

```bash
# 前端开发服务 (在 web 目录下)
cd web
pnpm dev

# 后端开发服务 (在 server 目录下)
cd server
pnpm start:dev
```

### 5. 构建项目

```bash
# 构建前端
cd web
pnpm build

# 构建后端
cd server
pnpm build
```

## 📝 开发指南

### 新增路由菜单

1. 在 `web/src/views` 目录下创建新的视图组件 `文件夹/index.vue`
2. 在 `系统管理 > 国际化 > menu` 中添加对应的多语言配置
3. 在 `系统管理 > 菜单管理` 中添加新菜单项
   - 参考已有菜单配置
   - 路由配置详情请参考 [Ant Design Pro 路由和菜单](https://pro.antdv.com/docs/router-and-nav)
4. 在 `系统管理 > 角色管理` 中为相应角色分配菜单权限
5. 保存并刷新页面，新菜单将会显示在导航中

## 🧩 功能模块
```
- 登录 / 注销

- 工作台

- 智能行政
  - 消息公告
  - 组织管理
  - 岗位管理
  - 组织架构

- 个人中心

- 功能页
  - 验证码
  - 自定义 Vue 指令
  - 懒加载
  - 瀑布流
  - 图片预览
  - 拾色器
  - 图片取色盘
  - 系统级取色器
  - Swiper
  - 打印
  - 文件预览
  - 拖拽

- 技术文档
  - Vue2
  - Nest.js
  - Ant Design Vue
  - Ant Design Pro

- 系统设置
  - 用户管理
  - 菜单管理
  - 角色管理
  - 国际化
  - 操作日志

- 关于

```

### 📚 技术文档快速访问

- [Vue2 文档](https://v2.cn.vuejs.org/)
- [Nest.js 文档](https://nestjs.com/)
- [Ant Design Vue 文档](https://1x.antdv.com/docs/vue/introduce-cn/)
- [Ant Design Pro 文档](https://pro.antdv.com/)

## 📸 系统截图

<table>
  <tr>
    <td><img src="./demo/1.png" alt="登录页面"></td>
    <td><img src="./demo/2.png" alt="工作台"></td>
  </tr>
  <tr>
    <td><img src="./demo/3.png" alt="消息公告"></td>
    <td><img src="./demo/4.png" alt="组织管理"></td>
  </tr>
  <tr>
    <td><img src="./demo/5.png" alt="岗位管理"></td>
    <td><img src="./demo/6.png" alt="组织架构"></td>
  </tr>
  <tr>
    <td><img src="./demo/7.png" alt="个人中心"></td>
    <td><img src="./demo/8.png" alt="功能页"></td>
  </tr>
  <tr>
    <td><img src="./demo/9.png" alt="用户管理"></td>
    <td><img src="./demo/10.png" alt="菜单管理"></td>
  </tr>
  <tr>
    <td><img src="./demo/11.png" alt="角色管理"></td>
    <td><img src="./demo/12.png" alt="国际化"></td>
  </tr>
  <tr>
    <td><img src="./demo/13.png" alt="操作日志"></td>
    <td><img src="./demo/14.png" alt="关于"></td>
  </tr>
</table>

## ⚠️ 注意事项

1. 本项目主要用于学习和交流，可能存在一些未经严格测试的功能点
2. 仅供个人学习和非商业用途使用
3. 欢迎通过以下方式参与项目改进：
   - 提交 [Issues](https://github.com/baiwumm/vue2-admin/issues) 反馈问题或建议
   - 提交 [Pull Requests](https://github.com/baiwumm/vue2-admin/pulls) 贡献代码

## 📄 许可证

本项目基于 [MIT许可证](./LICENSE) 开源。

## ⭐ Star 历史

[![Star History Chart](https://api.star-history.com/svg?repos=baiwumm/vue2-admin&type=Date)](https://star-history.com/#baiwumm/vue2-admin&Date)