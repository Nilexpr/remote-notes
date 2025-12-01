# React
summary:: 声明式 UI 库，通过组件描述界面状态

核心概念::

- Component :: React 的最小 UI 单元，接收 props 并返回 UI。
- useEffect :: 在浏览器绘制后执行副作用（异步边界）。
- Reconciliation :: Diff 算法：比较旧树/新树并应用最小更新。
- JSX :: JS 的语法糖，最终被编译成 createElement 调用。
  
  典型项目结构::
- src/components
- src/hooks
- src/pages
  
  解决的问题::
- 用状态描述 UI，避免手动同步 DOM
- 组件化可复用视图逻辑
  
  适用边界::
- 适合复杂业务界面
- 不适合：需要极致帧率的动画或游戏（考虑 WebGL）
  
  版本差异::
- 16 → 17：事件机制调整
- 17 → 18：Concurrent rendering 特性引入
  
  常见陷阱::
- useEffect 依赖写错导致无限循环
- 错误理解 setState 批处理行为
- summary:: 声明式 UI 库，通过组件描述界面状态