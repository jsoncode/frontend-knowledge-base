# 前端开发知识大纲

---

## 一、HTML

### [1. 基础与语义化](./frontend/1.1%20基础与语义化.md)
- HTML5 新增标签（`<section>`, `<article>`, `<nav>`, `<header>`, `<footer>`, `<aside>`, `<figure>`, `<figcaption>`）
- 语义化标签的意义与优势
- `<meta>` 标签常见用途（viewport、charset、description、keywords、http-equiv）
- `DOCTYPE` 声明的作用与模式（标准模式 vs 怪异模式）
- HTML 实体与字符编码

### [2. 表单与输入](./frontend/1.2%20表单与输入.md)
- 表单元素（`<input>`, `<textarea>`, `<select>`, `<button>`）
- HTML5 表单新属性（`required`, `placeholder`, `pattern`, `autofocus`, `autocomplete`）
- 新增输入类型（`email`, `number`, `date`, `range`, `color` 等）
- 表单验证机制（Constraint Validation API）
- 文件上传与 `FileReader` API

### 3. 多媒体与图形
- `<audio>` 和 `<video>` 标签使用
- Canvas 基本绘图 API
- SVG 与 HTML 集成
- `<picture>` 和 `<source>` 响应式图片

### 4. Web API 扩展
- Web Storage（`localStorage`, `sessionStorage`）
- Web Workers 基本使用
- Geolocation API
- Drag & Drop API
- Clipboard API

---

## 二、CSS

### 1. 样式基础
- 盒模型（标准 vs IE 盒模型，`box-sizing`）
- BFC（块级格式化上下文）原理与应用场景
- 层叠上下文（Stacking Context）与 `z-index`
- 选择器优先级计算
- CSS 继承与重置（`reset.css` vs `normalize.css`）

### 2. 布局技术
- 浮动（`float`）与清除浮动
- 定位（`position: static/relative/absolute/fixed/sticky`）
- Flexbox 布局（主轴与交叉轴、对齐方式、flex 属性）
- Grid 布局（网格容器、轨道、区域、对齐）
- 多列布局（`column-count`, `column-gap`）
- 响应式布局（媒体查询、移动优先设计）

### 3. 动画与过渡
- `transition` 过渡动画（属性、时间、缓动函数）
- `animation` 关键帧动画（`@keyframes`, 动画属性）
- `transform` 变换（2D/3D：`translate`, `rotate`, `scale`, `skew`）
- 动画性能优化（使用 `transform` 和 `opacity`）

### 4. 预处理器与工程化
- Sass/SCSS 特性（变量、嵌套、混合、继承、函数）
- Less 基本语法
- CSS Modules 与作用域隔离
- BEM 命名规范

### 5. 新特性与现代 CSS
- CSS 自定义属性（`--custom-property`）
- `:is()`, `:where()`, `:has()` 伪类
- `@container` 查询（Container Queries）
- `aspect-ratio` 属性
- `clamp()`, `min()`, `max()` 函数
- `:focus-visible`, `:focus-within`

### 6. 性能与优化
- 减少重排（reflow）与重绘（repaint）
- 使用 `will-change` 提示浏览器
- 避免强制同步布局（Layout Thrashing）
- 图片懒加载与 `loading="lazy"`

---

## 三、JavaScript

### 1. 基础语法
- 数据类型（原始类型 vs 引用类型）
- 类型检测（`typeof`, `instanceof`, `Object.prototype.toString`）
- 类型转换与隐式转换规则
- 作用域（全局、函数、块级）
- 闭包原理与应用场景
- `this` 指向机制（默认、隐式、显式、`new` 绑定）
- `call`, `apply`, `bind` 区别与实现

### 2. 函数与高阶编程
- 箭头函数特性（无 `this`, 无 `arguments`, 不能 `new`）
- 函数柯里化（Currying）与实现
- 节流（throttle）与防抖（debounce）实现
- 递归与尾递归优化

### 3. 对象与原型
- 构造函数与 `new` 的实现原理
- 原型链（`__proto__`, `prototype`, `constructor`）
- `Object.create()` 与原型继承
- ES6 类（`class`, `extends`, `super`）
- `Object.defineProperty()` 与数据劫持
- `Object.assign()`, `Object.keys()`, `Object.values()` 等方法

### 4. 异步编程
- 回调地狱与解决方案
- Promise 原理、状态、链式调用
- `Promise.all()`, `Promise.race()`, `Promise.allSettled()`
- async/await 语法与错误处理
- 事件循环（Event Loop）机制（宏任务 vs 微任务）
- 浏览器与 Node.js 事件循环差异

### 5. ES6+ 新特性
- `let`/`const` 与暂时性死区（TDZ）
- 解构赋值（数组、对象）
- 模板字符串与标签模板
- 默认参数、剩余参数、扩展运算符
- `Map`, `Set`, `WeakMap`, `WeakSet`
- `Symbol` 类型与内置 Symbol
- `Proxy` 与 `Reflect`（拦截操作、实现响应式）
- `Iterator` 与 `for...of`
- `Generator` 函数与异步流程控制

### 6. 模块化
- CommonJS（Node.js）
- AMD（RequireJS）
- ES Module（`import`/`export`，静态分析）
- 动态导入（`import()`）
- 模块打包与 Tree Shaking

### 7. 错误处理
- `try...catch` 与错误对象
- 全局错误监听（`window.onerror`, `window.addEventListener('error')`）
- `Promise` 错误捕获（`.catch`, `unhandledrejection`）
- Source Map 与错误定位

---

## 四、浏览器原理

### 1. 渲染机制
- 浏览器内核（WebKit, Blink, Gecko）
- DOM 树、CSSOM 树、渲染树构建
- 重排（reflow）与重绘（repaint）触发条件
- 合成（compositing）与图层（layer）

### 2. 关键渲染路径（Critical Rendering Path）
- 构建 DOM
- 构建 CSSOM
- 生成渲染树
- 布局（Layout）
- 绘制（Paint）
- 合成（Composite）

### 3. 存储机制
- Cookie（大小、过期、安全属性）
- localStorage / sessionStorage
- IndexedDB（事务、索引、游标）
- Cache API（Service Worker 使用）
- Storage 事件监听

### 4. 安全机制
- 同源策略（SOP）
- 跨域解决方案（CORS、JSONP、postMessage、代理）
- XSS（跨站脚本攻击）类型与防御
- CSRF（跨站请求伪造）原理与防护（Token、SameSite）
- CSP（内容安全策略）配置
- HTTPS 与混合内容（Mixed Content）

### 5. 网络与性能
- HTTP/1.1 vs HTTP/2 vs HTTP/3 特性
- TCP 三次握手、四次挥手
- DNS 解析过程
- 缓存机制（强缓存 `Cache-Control`, `Expires`；协商缓存 `ETag`, `Last-Modified`）
- Preload, Prefetch, Preconnect, DNS-Prefetch
- 懒加载（图片、组件）
- 骨架屏与 SSR/SSG 优化首屏

---

## 五、前端框架（以 React 为主，兼顾 Vue）

### 1. React
- 核心概念（组件、JSX、虚拟 DOM）
- 函数组件 vs 类组件
- React Hooks（`useState`, `useEffect`, `useContext`, `useReducer`, `useCallback`, `useMemo`, `useRef`）
- 状态管理（Context API、Redux、Redux Toolkit、Zustand）
- React Router（动态路由、嵌套路由、编程式导航）
- 错误边界（Error Boundary）
- Portals 使用场景
- Concurrent Mode 与 Suspense
- React 18 新特性（自动批处理、Transition API）
- 性能优化（React.memo, useCallback, useMemo, Profiler）

### 2. Vue
- 核心概念（响应式原理、模板、指令）
- Vue 2 vs Vue 3 差异（Proxy vs Object.defineProperty）
- Composition API（`setup`, `ref`, `reactive`, `computed`, `watch`）
- 生命周期钩子（选项式 vs 组合式）
- Vuex / Pinia 状态管理
- Vue Router（路由守卫、懒加载）
- Teleport 与 Suspense
- 自定义指令与插件开发

### 3. 框架通用
- 虚拟 DOM Diff 算法原理（双端比较、key 作用）
- 组件通信方式（props、事件、context、状态管理、事件总线）
- 高阶组件（HOC）与 Render Props
- 插槽（Slot）机制（默认、具名、作用域插槽）

---

## 六、工程化与构建工具

### 1. 构建工具
- Webpack 核心概念（入口、出口、loader、plugin、mode）
- 常见 Loader（babel-loader, css-loader, file-loader, url-loader）
- 常见 Plugin（HtmlWebpackPlugin, MiniCssExtractPlugin, DefinePlugin）
- Tree Shaking 原理与配置
- Code Splitting（按路由、按组件、vendor 分离）
- 懒加载（动态 `import()`）
- HMR（热模块替换）原理
- Webpack 5 新特性（持久化缓存、Module Federation）

- Vite 原理（ESM + 原生 ES Modules + Rollup 打包）
- Vite 与 Webpack 对比
- Rollup 特点（适合库打包）
- Parcel 零配置特性

### 2. 包管理
- npm / yarn / pnpm 对比
- `package.json` 字段详解（`scripts`, `dependencies`, `devDependencies`, `peerDependencies`）
- Semantic Versioning（语义化版本）
- Monorepo 管理（Lerna, Turborepo, Nx）

### 3. 代码质量
- ESLint 配置与规则定制
- Prettier 代码格式化
- Husky + lint-staged 提交前检查
- TypeScript 集成
- 单元测试（Jest, Vitest）
- E2E 测试（Cypress, Playwright）

---

## 七、TypeScript

### 1. 基础类型
- 原始类型（`string`, `number`, `boolean`）
- 数组、元组、枚举、any、unknown、never、void
- 接口（`interface`）与类型别名（`type`）
- 函数类型定义

### 2. 高级类型
- 联合类型（`|`）与交叉类型（`&`）
- 类型守卫（`typeof`, `instanceof`, `in`, 自定义类型谓词）
- 泛型（`<T>`）与约束（`extends`）
- 映射类型（`Partial`, `Readonly`, `Pick`, `Record`）
- 条件类型（`T extends U ? X : Y`）
- 模板字面量类型

### 3. 面向对象
- 类（`class`）、继承、访问修饰符（`public`, `private`, `protected`）
- 抽象类与接口
- 装饰器（`@decorator`）支持（需配置）

### 4. 工程集成
- 与 React/Vue 集成（类型定义 `.d.ts`）
- `tsconfig.json` 关键配置
- 类型声明文件管理

---

## 八、性能优化

### 1. 加载性能
- 减少请求数（合并、雪碧图、内联）
- 压缩资源（Gzip, Brotli）
- CDN 加速静态资源
- 关键资源预加载（preload, prefetch）
- 懒加载非关键资源

### 2. 运行时性能
- 避免内存泄漏（闭包、事件监听、定时器）
- 使用 `requestIdleCallback`, `requestAnimationFrame`
- 防抖节流优化事件处理
- 虚拟列表（Virtual List）实现长列表
- Web Workers 处理复杂计算

### 3. 监控与分析
- Performance API（`performance.now()`, `mark`, `measure`）
- Lighthouse 审计
- Chrome DevTools 使用（Performance、Memory、Coverage 面板）
- 前端监控（错误日志、性能上报、PV/UV 统计）

---

## 九、服务端与全栈基础

### 1. Node.js
- 核心模块（`fs`, `path`, `http`, `events`, `stream`）
- Express/Koa 框架基础
- 中间件机制
- RESTful API 设计
- JWT 认证流程
- 文件上传处理

### 2. SSR 与同构
- SSR 原理与优势（SEO、首屏快）
- Next.js / Nuxt.js 框架使用
- 数据预取（`getServerSideProps`, `getStaticProps`）
- CSR vs SSR vs SSG vs ISR

### 3. 服务端通信
- REST API 设计规范
- GraphQL 基础（查询、变更、Schema）
- WebSocket 实时通信
- Server-Sent Events (SSE)

---

## 十、设计模式与架构

### 1. 常见设计模式
- 单例模式
- 观察者模式（Event Emitter）
- 发布-订阅模式
- 工厂模式
- 代理模式（Proxy 实现响应式）
- 中介者模式

### 2. 前端架构
- MVC / MVVM 模式理解
- 组件化设计原则（单一职责、可复用、可测试）
- 微前端架构（qiankun、Module Federation）
- 状态管理架构（Redux、MobX、Zustand）
- 前后端分离与接口规范

---

## 十一、面试高频场景题

### 1. 手写代码题
- 实现 `Promise`（all, race, finally, resolve, reject）
- 实现 `bind` / `call` / `apply`
- 实现深拷贝（考虑循环引用、函数、Symbol）
- 实现节流/防抖
- 实现 EventEmitter
- 实现 `new` 操作符
- 实现 `instanceof`
- 实现 `JSON.stringify` / `JSON.parse` 简化版
- 实现数组扁平化、去重、排序
- 实现柯里化函数

### 2. 场景设计题
- 设计一个图片懒加载组件
- 实现一个无限滚动列表
- 设计一个表单校验系统
- 实现一个前端路由（hash / history）
- 设计一个权限控制系统
- 实现一个消息通知中心
- 设计一个埋点系统

### 3. 性能优化实战
- 白屏时间过长如何排查？
- 页面卡顿如何分析？
- 如何减少 bundle 体积？
- 如何优化首屏加载速度？

---

## 十二、软技能与项目经验

- 项目架构设计经验
- 团队协作与代码评审（Code Review）
- 技术选型依据
- 问题排查思路（从现象到根因）
- 沟通能力与文档编写
- 技术分享与团队成长

---

> **备注**：此大纲适用于 **资深前端工程师** 面试准备，覆盖广度与深度。建议结合实际项目经验深入理解每个知识点，并能清晰表达设计思路与权衡取舍。
