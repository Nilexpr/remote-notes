summary:: 声明式 UI 库，通过组件描述界面状态
core-concepts:: [[Component]] [[Hook]] [[Reconciliation]] [[JSX]]

典型项目结构::

- src/components
- src/hooks
- src/pages
  
  解决的问题::
- 用状态描述 UI，避免手动同步 DOM
- 组件化可复用视图逻辑
  
  适用边界::
- 适合复杂业务界面
- 不适合：极端高帧率动画或游戏（考虑 WebGL）
  
  版本差异::
- 16 → 17：事件委托机制调整
- 17 → 18：引入 Concurrent rendering
  
  常见陷阱::
- useEffect 依赖写错导致无限循环
- 错误理解 setState 批处理行为