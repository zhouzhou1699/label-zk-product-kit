# 原型说明

## 怎么打开

双击 `index.html`（纯静态、无依赖、无网络请求），左侧导航切换页面，或直接访问：

```
index.html#home       首页
index.html#capacity   产能看板（全新）
index.html#projects   项目列表
index.html#tasks      任务管理器
index.html#annotate   标注工作台
index.html#rewards    积分
index.html#market     模型超市
index.html#dashboard  数据大屏
```

## 原型覆盖了什么

| 页面 | 类型 | 关键改造 |
|---|---|---|
| 首页 | 改造 | 「待办（按影响排序）」替代纯公告；StatCard 带 scope chip |
| **产能看板** | **全新** | 漏斗 + 瓶颈诊断 + ETA + 按人负载 + 通过/新增对比 |
| 项目列表 | 改造 | 三段式进度、草稿计数、通过率措辞、紧凑卡 |
| 任务管理器 | 改造 | StatusPill 六态、草稿滞留黄条、打回原因、验收分数 |
| 标注工作台 | 改造 | 统一顶栏、「打回」第 4 页签、叠加对比、提交主色 |
| 积分 | 改造 | 流水展开计分构成、打回即时扣分、距证书差值 |
| 模型超市 | 改造 | 多选对比、平台采纳率 |
| 数据大屏 | 改造 | 与浅色共用 token、瓶颈结论、KPI scope |

## 设计与实现约定

1. **单一 token 源**：所有颜色/字号/间距来自 `../03-design/tokens.css`，页面内不写死色值。
2. **两主题**：`data-theme="light"`（外壳与标注页）与 `data-theme="dark"`（大屏），同一套变量名。
3. **六态固定映射**：`unclaimed / working / drafting / pending_review / pending_validation / passed / rejected` 的色与词在全站一致，见 `03-design/01-设计系统.md §2.4`。
4. **每个数字都有 scope**：`<span class="scope" data-scope="TEAM">` 三档（TEAM / INSTITUTION / PLATFORM）+ SELF。
5. **禁用必写原因**：任何 `disabled` 按钮都有 `title`，对应真实产品里"为什么模型是灰的"这条最佳实践。

## 与真实产品的差异（诚实的部分）

| 项 | 原型 | 真实产品 |
|---|---|---|
| 数据 | 取自 2026-11-14 实测（8 单位/47 项目/4,825 任务等） | 同源，但原型里混入了 v2 假设值（如"草稿 2 条""采纳率 62%"） |
| 图表 | CSS 手绘（柱/环） | ECharts 或自研 canvas |
| 交互 | 页面切换、segmented 点选、页签点选 | 完整 CRUD、拖拽、键盘导航 |
| 标注画布 | 静态图 + 一个示意框 | Label Studio 完整画布（25 种范式） |
| 字段校验 | 无 | 完整表单校验与错误提示 |

> 原型目的是**对齐"改成什么样"**，不是可交付代码。工程实现请看 `03-design/02-页面规格说明.md` 与 `01-analysis/06-接口清单与数据字典.md`。

## 分屏截图

`../05-assets/prototype/P1..P8-*.png`（1600×1000，整页截图）。
