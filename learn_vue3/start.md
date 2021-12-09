### ch01

#### 涉及哲学

- 渐进式框架

  框架本身有复杂度

  声明式渲染 -> 组件系统 -> 路由 -> 状态管理 -> 构建工具

- 构建用户界面

  - 渲染机制
    - 完全的动态渲染  优点：灵活，virtual dom的表现力 缺点：运行时臃肿
    - 模板渲染 优点：编译时可以增加优化点 缺点：没有virtual dom,表现力匮乏
  - vue的选择
    - 保留virtual dom的表现力。同时保留模板渲染和render动态渲染

- 数据驱动

  - UI = f(data)   vue正式要完成这一个映射。 数据即视图。 视图即数据

- 总结：vue关注视图层。 提供了一种响应式的描述UI的一种方式

  [视频](https://www.bilibili.com/video/BV134411c7Sk)

#### UI

- 数据 视图  行为

- 数据（属性，状态） 视图  行为

- 属性，视图  行为状态 

- 属性，视图  状态行为 作用行为 上下文

  [组合式api](https://v3.cn.vuejs.org/guide/composition-api-introduction.html#%E4%BB%A3%E7%A0%81%E7%BB%84%E7%BB%87)

  [React hooks实战指南](https://www.bilibili.com/video/BV1Ge411W7Ra)

#### vue 的内在

- reactivity响应式系统

  依赖收集和派发更新， 每个组件一个watcher实例，组件级响应

- runtime运行时系统

  runtime-core   render函数 -> virtual dom

  runtime-dom   virtual dom -> dom

- complier 编译器

  模板 -> render函数

