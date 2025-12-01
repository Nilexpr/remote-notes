summary:: 声明式 UI 库，通过组件描述界面状态
核心概念:: [[Component]], [[Hook]], [[Reconciliation]], [[JSX]]
典型项目结构:: src/components, src/hooks, src/pages
解决的问题::

- 用状态描述 UI，避免手动同步 DOM
- 组件化可复用视图逻辑
  
  适用边界::
- 适合复杂业务界面
- 需要频繁状态更新的交互
- 不适合：极端高性能动画、游戏（需 WebGL）
- 版本差异::
	- 16 → 17：事件委托机制变更
	- 17 → 18：添加 concurrent rendering / Suspense SSR
	  
	  常见陷阱::
- useEffect 依赖写错导致无限循环
- State 更新批处理规则误解