# 素材索引

## 一、`annotated/` —— 带标注的设计走查图（11 张）

真实界面截图 + 编号热点框 + 右侧问题/建议面板。每张图都是"看到问题 → 知道怎么改"。

| 文件 | 页面 | 核心结论 |
|---|---|---|
| [A01-项目列表.png](annotated/A01-项目列表.png) | 项目列表 | 同名指标三种口径（47 / 80 / 95）；进度口径与状态机不一致 |
| [A02-任务管理器.png](annotated/A02-任务管理器.png) | 任务管理器 | 页签即流程（好）；状态列无统一色板；缺草稿滞留维度 |
| [A03-数据集库.png](annotated/A03-数据集库.png) | 数据集库 | 47 节点分类树无搜索；直链 `/datasets/new` 返回 503 |
| [A04-标注奖励积分.png](annotated/A04-标注奖励积分.png) | 积分 | 流水只给 +13 不给构成；空态占掉首屏 1/8 |
| [A05-模型超市.png](annotated/A05-模型超市.png) | 模型超市 | 四道准入关卡写得好；缺产线证据（采纳率）与横向对比 |
| [A06-数据大屏.png](annotated/A06-数据大屏.png) | 数据大屏 | KPI 有值无结论；交付率 3.9% 无诊断；主题未共享 token |
| [A07-系统管理RBAC.png](annotated/A07-系统管理RBAC.png) | 权限矩阵 | 107 码 × 26 类 × 三态 + 效果预览（完成度高）；缺搜索与反查 |
| [A08-组织管理.png](annotated/A08-组织管理.png) | 组织管理 | 表格一格塞三行信息，无法扫读/排序 |
| [A09-模型训练.png](annotated/A09-模型训练.png) | 模型训练 | 集群状态透明；曲线无暂停；训练完的去处无链接 |
| [A10-登录页.png](annotated/A10-登录页.png) | 登录页 | **P0 验证码可绕过**；价值主张三连是最强文案资产 |
| [A11-标注工作台.png](annotated/A11-标注工作台.png) | 标注工作台 | 顶栏与外壳割裂；缺打回历史；提交按钮被弱化 |

> 生成方式：`_tools/annotate_design.py`（读取 `_src/vp-*.png` + 手工标定的热点坐标）。

## 二、`screens/` —— 真实界面截图（30 张）

全部来自 2026-11-14 的实际登录抓取，1600px 宽，部分整页。

| 文件 | 页面 | 备注 |
|---|---|---|
| 01-login.png | 登录 | 含滑块拼图验证码 |
| 02-home.png | 首页工作台 | 4 指标 + 公告 + 快捷入口 |
| 03-dashboard.png | 数据大屏 | 深色，6 KPI + 趋势 + 交付率 |
| 04-projects.png | 项目列表 | 整页 3360px（含 20+ 项目卡） |
| 05-task-manager.png | 任务管理器 | 身份切换 + 六态计数 |
| 06-annotate.png | 标注工作台 | 画布 + 区域面板 + 提交 |
| 07-project-roles.png | 角色设置 | 前置条件 4 项 + 三角色 |
| 08-project-settings.png | 项目设置 | 7 个面板 |
| 09-project-stats.png | 数据统计 | 六状态分布 |
| 10-export.png | 数据导出 | 格式按 label_config 动态 |
| 11-publish.png | 项目发布 | 四项检查（最佳设计） |
| 12-project-rewards.png | 项目奖励 | 总览 + 规则 |
| 13-datasets.png | 数据集库 | 47 节点分类树 |
| 14-dataset-new.png | 新建数据集弹层 | 可见性四选一 |
| 15-training-sets.png | 训练集库 | 18 个训练集 |
| 16-training.png | 模型训练 | AMD 8 卡 + 实时曲线 |
| 17-market.png | 模型超市 | 21 在架 + 本周精选 |
| 18-market-drawer.png | 模型详情抽屉 | 基准评测 + 版本记录 |
| 19-app-embodied.png | 模型应用 · 具身智能 | 6 类本体 |
| 20-app-industrial-qc.png | 模型应用 · 工业质检 | 99.7% 检出率 |
| 21-app-campus.png | 模型应用 · 校园安防 | 192 台设备 |
| 22-app-tea.png | 模型应用 · 茶叶工控 | 环境/虫情/视觉 |
| 23-points.png | 积分 | 403 分 + 流水 |
| 24-certificates.png | 我的证书 | 空态 |
| 25-certificate-center.png | 证书中心 | PDF 真实预览 |
| 26-org-admin.png | 组织管理 | 8 单位表格 |
| 27-requests.png | 申请审批 | 127 条（97 已驳回） |
| 28-rbac.png | 系统管理 | 权限矩阵 |
| 29-platform-settings.png | 超管设置 | 登录页品牌 |
| 30-labeling-templates.png | 标注模板库 | 25 种范式 |

## 三、`prototype/` —— v2 高保真原型渲染图（8 张）

| 文件 | 页面 | 状态 |
|---|---|---|
| P1-首页.png | 首页 | 改造 |
| P2-产能看板.png | 产能看板 | **全新** |
| P3-项目列表.png | 项目列表 | 改造 |
| P4-任务管理器.png | 任务管理器 | 改造 |
| P5-标注工作台.png | 标注工作台 | 改造 |
| P6-积分.png | 积分 | 改造 |
| P7-模型超市.png | 模型超市 | 改造 |
| P8-数据大屏.png | 数据大屏 | 改造 |

可点版本：`../04-prototype/index.html`

## 四、其它

- `canvas-sample.jpg`：标注画布示例图（从真实截图裁切，用于原型画布）。
- `_src/vp-*.png`：标注图生成源（1600×1000 视口截图）。
