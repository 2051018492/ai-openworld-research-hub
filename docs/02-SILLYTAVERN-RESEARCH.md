# DeepSeek Pro｜SillyTavern 技术复用与底座选型研究

> 工作类型：开源源码审计、架构对比、条件允许时的隔离 PoC。只研究，**不修改私有应用**。不得接触生产服务器或在无授权情况下使用付费 AI API。

## 研究目标

- https://github.com/SillyTavern/SillyTavern
- https://github.com/Soyo5800/rpg-tracker-for-sillytavern
- https://github.com/virgilianshailer/story-tracker
- https://github.com/StygianTechnica/SillyTavern-StateEngine
- https://github.com/lilminzyu/ST-StatusTracking
- REA https://rea.tools/ （可选；优先直接分析开源源码）

## A. 实际源码审计

找出确切版本/提交和源代码位置，检查：

- 角色卡、世界书、提示词与模型 API；
- 群聊、上下文、历史、摘要与向量检索；
- 聊天分支、Swipe、重生成、删除与存储；
- 变量、STscript、扩展事件与插件依赖；
- 状态栏的数据结构、解析、校验、持久化、历史回滚；
- 服务器认证、数据隔离、Node/Docker 部署与安全。

每项明确区别 **文档功能声明**、**实际源码验证**、**运行测试结果**。

## B. 三种路线的对比

| 方案 | 描述 |
|---|---|
| A | 以 SillyTavern 为底座，增加独立世界运行机制 |
| B | 保留已有 Node + SQLite 世界引擎，依法复用成熟聊天/状态组件 |
| C | SillyTavern 交互 UI 与独立的世界事件服务集成 |

重点比较模块复用程度、代码依赖、事件/状态一致性、NPC 私有知识、许可义务、服务器安全、移动端体验、长期升级成本；禁止编造精确工时或节省比例。

## C. 最小隔离 PoC（条件允许才运行）

1. 新建空白角色卡；
2. 自定义 Number、Text、Enum 字段；
3. 从一次交互产生有效状态变化，检查真实持久化；
4. 删除/重新生成/分支一条消息，检查状态回滚；
5. 两位角色具有不同私人知识，不应自动互相知晓；
6. 检查 UI 状态、实际存储与下一轮 AI 上下文是否一致。

不支持的实验必须明确写「未运行」，不可冒充完成。优先使用虚拟数据和 mock 模型。

## D. 交付文件

建议通过研究分支 PR 交付 `docs/research/` 内的：
- `SILLYTAVERN-SOURCE-AUDIT.md`
- `PLUGIN-REUSE-MATRIX.md`
- `ISOLATED-POC-RESULTS.md`
- `BASE-ARCHITECTURE-DECISION-MEMO.md`

每份提供版本、源码证据、依赖/许可证、可复现步骤、限制、明确结论。请勿复制大量第三方原始源码到报告，也不可粘贴私有项目文件。

**研究者提供建议；主脑与用户做最终技术决策。**