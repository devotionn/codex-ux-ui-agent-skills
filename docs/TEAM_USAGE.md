# Codex UX/UI Skills｜团队设计使用指南

这份文档面向公司内部的产品设计师、UI/UX 设计师、产品经理和前端同事。

目标不是让每个人学习十几个 Skill，而是把 `$product-design` 作为统一入口，让 Codex 根据任务自动加载更窄的设计能力。

## 1. 推荐的团队使用方式

### 方式 A：项目级安装（团队默认，推荐）

把本仓库的 `.agents/skills/` 放进实际产品仓库根目录的 `.agents/skills/` 并提交到 Git。

这样任何人在该产品仓库里启动 Codex，都能获得同一套设计 Skill；团队版本也可以随代码一起审查和升级。

适合：公司正式产品、多人协作、需要稳定版本的项目。

### 方式 B：个人级安装

Codex 也支持用户级 Skill。可以通过 `$skill-installer` 从 GitHub 仓库安装，或把 Skill 放到 `$HOME/.agents/skills/`。

安装后在 Codex 中运行 `/skills`，确认能看到 `product-design`、`design-screen`、`redesign`、`design-review` 等 Skill。

如果新安装内容没有立即出现，重启 Codex 再检查。

## 2. 设计同事只需要记一个入口

优先显式调用：

```text
$product-design
```

然后直接讲业务任务，不需要指定底层 Skill。

例如：

```text
$product-design
帮我重新设计这个报价工作台页面。
先理解现有业务逻辑和用户操作路径，不要删功能；
重点优化信息层级、关键操作、表格密度、状态反馈和移动端适配。
如果项目能运行，请实际渲染并检查后再给结果。
```

Codex 会根据任务选择 `design-screen`、`redesign`、`design-component`、`accessibility-audit`、`design-review`、`ship` 等能力。

## 3. 常用设计任务模板

### 新页面

```text
$product-design
根据这个需求设计并实现一个新的订单详情页。
先检查现有导航、组件库、token 和数据结构；
保持现有产品风格，覆盖 loading / empty / error / permission / success 状态；
完成后检查桌面端和窄屏，并做一次设计 review。
```

### 改版现有页面

```text
$product-design
重构这个页面的 UI/UX，但不要改业务逻辑、API、校验和已有操作。
先说明当前主要问题，再做改版；
不要做成通用 AI Dashboard 风格，要延续产品现有设计语言。
```

### 只做设计评审，不改代码

```text
$product-design
只做 review，不修改代码。
实际运行并查看这个页面，检查信息层级、密度、可读性、操作可发现性、状态表达、响应式和无障碍。
按优先级给出证据和修改建议，不要用主观打分。
```

### 根据截图优化

```text
$product-design
参考我提供的截图提取布局、层级和视觉规律，结合当前项目已有组件和 token 重新实现。
不要机械复制素材，也不要为了像截图而破坏当前产品功能。
```

### 交付前检查

```text
$ship
对这次 UI 改动做最终 handoff 检查：
review diff → tests → render → responsive → states → keyboard/focus → final critique。
最终明确写 Implemented / Verified / Not verified / Remaining。
```

## 4. 每个产品仓库最好补一份自己的设计上下文

Skill 负责通用工作流，但公司的具体品牌和产品规范应该放在目标产品仓库自己的 `AGENTS.md` 或设计文档里。

建议至少记录：

- 产品是什么、核心用户是谁、核心任务是什么
- 当前前端框架和组件库
- 设计 token / theme 的位置
- 品牌色、字体、图标和语气规范
- 不允许破坏的业务逻辑、权限和数据契约
- 关键页面/组件的位置
- 支持的桌面端、移动端、主题和浏览器范围
- 可访问性目标
- 可用于 render / test / screenshot 的命令

不要把所有资料塞进一个巨大的 `AGENTS.md`。让 `AGENTS.md` 做地图，把详细规范放在可按需读取的文档里。

## 5. 设计师和工程师的边界

### 设计师可以直接让 Codex 做

- 页面/组件方案
- 页面改版
- UI consistency audit
- 设计 review
- UX writing
- responsive / state 设计
- accessibility review
- 在现有前端代码基础上直接实现和验证 UI

### 遇到这些情况要保留人工 Owner 决策

- 品牌方向发生重大变化
- 业务流程或权限逻辑要改变
- API / 数据模型需要变化
- 引入新的 UI 框架或第二套设计系统
- 关键用户路径有不可逆改动
- 设计要求与业务、安全、合规约束冲突

## 6. 团队验收标准

一个 UI 任务不能只因为“看着更漂亮”就算完成。

至少区分：

- **Implemented**：真正改了什么
- **Verified**：真正运行、测试、渲染和检查了什么
- **Not verified**：哪些能力因为环境限制没有验证
- **Remaining**：还剩什么问题或 Owner 决策

对于只做设计不改代码的任务，则输出 Direction / Structure / States & accessibility / Handoff。

## 7. 推荐团队约定

公司内部可以统一约定：

> 所有较大的 UI/UX 任务默认从 `$product-design` 开始；需要专项工作时再直接调用 `$design-review`、`$accessibility-audit` 或 `$ship`。

这样设计同事只需要掌握一个入口，而工程侧仍保留细粒度 Skill 能力。
