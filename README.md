# AI 开放世界｜公开研究与交流仓库

> **这是公开技术研究与交流仓库，不是 AI 开放世界软件的主代码仓库。** 本仓库用于让 DeepSeek Pro 等研究工具在无需访问私人仓库的情况下，阅读公开需求、研究 SillyTavern（酒馆）与状态插件、提出可验证的架构建议。
>
> **尚未决定迁移 SillyTavern。** 不上传私有源码、凭据、生产信息、私人聊天、未审查截图或第三方项目完整代码。

## 产品目标

- **角色卡聊天模式**：不必先创建世界；可直接导入或创建角色卡聊天，按需使用记忆、世界书、状态栏和群聊。
- **开放世界模式**：世界和规则由用户定义；NPC 有稳定身份、状态、事件、关系、知识边界、时间及有预算的自主行为。
- **核心体验**：交互的后果被可靠持久化，并反映在状态栏、人物资料、场景、后续对话中，而不是只让模型在聊天文本中编造变化。

## DeepSeek Pro：从这里开始

1. 阅读 [中文接棒说明](docs/05-DEEPSEEK-PRO-START-HERE-中文.md)。
2. 阅读 [具体研究任务](docs/02-SILLYTAVERN-RESEARCH.md)。
3. 参考 [产品范围](docs/01-PRODUCT-SCOPE.md) 和 [决策状态](docs/03-ARCHITECTURE-DECISIONS.md)。
4. 按 [报告模板](docs/04-RESEARCH-RESULT-TEMPLATE.md) 提交研究结果。

## 交流方式

- **GitHub Issues**：提出研究问题、记录有证据支持的发现与待主脑决策事项。
- **Pull Requests**：提交架构研究报告、技术对比和可重现的隔离实验。
- **docs/research/**：存放研究 Agent 产出的结果（报告经审查后进入主分支）。

## 安全与权限

此仓库**不代表有权访问私有开发仓库**。需要阅读实际私有应用源码时，必须另由用户提供经过安全审查的源码包。当前 Astra 的 V0.6 工作不能中断、不能覆盖；本研究也不授权修改腾讯云生产环境、运行未经授权的付费 API 测试或合并任何开发 PR。

[贡献与资料安全规则](CONTRIBUTING.md)

外部研究资料：[SillyTavern](https://github.com/SillyTavern/SillyTavern) · [RPG Tracker](https://github.com/Soyo5800/rpg-tracker-for-sillytavern) · [Story Tracker](https://github.com/virgilianshailer/story-tracker) · [State Engine](https://github.com/StygianTechnica/SillyTavern-StateEngine) · [ST-StatusTracking](https://github.com/lilminzyu/ST-StatusTracking)

**许可证说明：**本公开研究仓库尚未对原创应用程序源码授予开源许可证；研究中引用的外部开源项目按各自许可证处理。