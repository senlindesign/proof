[English](README.md) | [中文](README.zh-CN.md)

# Proof

![Proof — 产品设计技能](docs/images/cover.png)

### 一个产品设计技能

[![Website](https://img.shields.io/badge/Website-proofdesign.dev-1F5EFF?style=flat-square)](https://proofdesign.dev/zh)
[![Made for Claude Code](https://img.shields.io/badge/Made%20for-Claude%20Code-blueviolet?style=flat-square&logo=anthropic)](https://docs.anthropic.com/en/docs/claude-code)
[![Made for Codex](https://img.shields.io/badge/Made%20for-Codex-000000?style=flat-square&logo=openai)](https://openai.com/index/introducing-codex/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

**做出来的页面像真实上线的产品，不像 AI 生成的。所有做法都来自 400 多个真实产品页面。**

Proof 是一个产品设计技能，可以在 Claude Code 和 Codex 里用。告诉它你要哪个页面，它就做出一个完整的响应式页面：首屏有真实感的产品展示，有鲜明的视觉风格，动效展示的是产品在工作的样子。8 类页面、10 类区块、4 种风格，深浅两色都有。

**在线看效果 → [proofdesign.dev](https://proofdesign.dev/zh)**：上面每一个页面都是这个技能生成的，点开就能滚动、悬停、随手点点。

## 30 秒上手

```bash
npx skills add senlindesign/proof
```

装好后对 Agent 说：

```text
/proof landing
/proof pricing editorial dark
/proof landing — Patchwork，给小型设计工作室用的共享灵感板
```

其他安装方式见[下面](#安装)。

---

## 风格

*同一个需求（"Relay，给客服团队用的共享收件箱"）在四种风格下的首屏。点图片可以打开在线页面。*

| Minimal | Business |
| --- | --- |
| [![Minimal](docs/images/style-minimal.png)](https://proofdesign.dev/style-minimal-relay) | [![Business](docs/images/style-business.png)](https://proofdesign.dev/style-business-relay) |
| **Colorful** | **Editorial** |
| [![Colorful](docs/images/style-colorful.png)](https://proofdesign.dev/style-colorful-relay) | [![Editorial](docs/images/style-editorial.png)](https://proofdesign.dev/style-editorial-relay) |

| 风格 | 性格 | 招牌首屏 |
| --- | --- | --- |
| **Minimal**（默认） | 黑白灰，不用阴影，边角锐利 | 细线网格的"标本场"，中间一个主产品画面 |
| **Business** | 温暖可信，柔和阴影，圆角 | 多色渐变舞台上的产品界面，带功能标签 |
| **Colorful** | 活泼有手作感，衬线标题，纸感卡片 | 飘着网点云的天空，升起一张纸质产品页 |
| **Editorial** | 有作者感、沉静，大号衬线，一个青色点缀 | 深色"报纸头版"，配一扇纸质产品窗口 |

每种风格都是用 [Taste Lab](https://github.com/senlindesign/taste-skill) 从一个真实产品网站里提取的，深浅两色都有，也都能搭配任何页面类型。

---

## 它强在哪

1. **学自真实产品，不是模型自己的审美。** 通过 [Mobbin](https://mobbin.com) 的 MCP 研究了 400 多个上线页面，每个做法都写了原因，也写了什么时候不该用。
2. **四种风格，各有性格。** 每种都有自己的首屏、质感和动效。换一种风格是另一个设计，不是换个颜色。
3. **首屏里是真实感的产品。** 有人名、状态、数字，绝不是灰色占位框。
4. **整个官网能做，一个区块也能做。** 可以要完整的落地页，也可以只要价格表、FAQ 或页脚。
5. **接得住你的品牌和内容。** 有多少给多少。没给的用完整的示例内容补上，QA 报告会列出每一处，方便替换。
6. **交给你之前先自己检查。** 检查布局节奏、风格是否到位、logo 是否真实、有没有编造的事实，再告诉你哪些通过了。

**它会避开的东西**：AI 页面最常见的样子。同一个居中模板从上重复到下 · 三张一模一样的功能卡片 · 灰色占位框和手画 logo · 蓝紫两色渐变 · 把编造的内容当成事实 · 所有内容都淡入上移。

### 产品设计的五个层次

大多数设计技能只决定页面长什么样。Proof 还决定页面放什么、按什么顺序放，因为它学的是 400 多个已经上线、经过市场验证的产品页面。分层出自 Jesse James Garrett 的《用户体验要素》。

| 层次 | 它决定什么 |
| --- | --- |
| **战略层**（推断） | 页面给谁看，要让他们做什么：从你的需求里读出来，再对照已经跑通的页面。Proof 不替你做战略。 |
| **范围层** | 放哪些区块，不放哪些 |
| **结构层** | 区块的先后顺序，以及布局怎么交替 |
| **框架层** | 每个区块内部怎么排 |
| **表现层** | 风格、质感和动效 |

所以同一个产品，可以得到两个不同的页面：给想马上试用的开发者，是一个短页面（首屏、功能、注册）；给不了解这类产品的 IT 总监，会加上问题说明、工作原理和安全说明。

---

## 能做什么

[![9 种页面配置](docs/images/configs.jpg)](https://proofdesign.dev/zh#pages)

| 页面类型 | 用途 | Archetype |
| --- | --- | --- |
| **Landing** | 向新访客介绍你的产品 | SaaS Tool · SaaS Platform · Developer Tool · Creative Tool |
| **Pricing** | 套餐和收费方式 | Feature-Tiered · Usage-Based · Simple Binary · Enterprise-First |
| **Product** | 给正在评估的人细讲功能 | Feature Showcase · Platform Overview · Product Deep-Dive |
| **About** | 公司和团队的故事 | Company Story · Team-First · Mission-Driven |
| **Contact** | 咨询、支持、预约演示 | Simple Contact · Department Routing · Sales-Focused · Support Hub |
| **Blog** | 文章和更新日志 | Grid Index · Editorial · Minimal List |
| **Downloads** | 桌面应用、命令行工具、SDK | Platform Selector · Multi-Product · Developer Distribution |
| **404** | 帮走丢的访客找到路 | Minimal Redirect · Navigational Recovery · Brand Moment |

[![10 类区块](docs/images/sections.jpg)](https://proofdesign.dev/zh#sections)

每个页面还自带：8 种真实感的产品展示配方、17 种在真实网站上见过的招牌布局、取自风格色板的氛围质感、展示产品在工作的动效（尊重系统的"减少动态效果"）、来自图标库的真实 logo，以及按 72 条真实标题总结出的文案写法。

---

## 安装

| 在哪用 | 怎么装 |
| --- | --- |
| **任意 Agent，一行命令** | `npx skills add senlindesign/proof`（[skills.sh](https://skills.sh) 会问你装到哪个 Agent） |
| **Claude Code 插件** | `/plugin marketplace add senlindesign/proof`，再 `/plugin install proof@proof`。用的时候输入 `/proof:proof`，用 `/plugin update` 更新。 |
| **Claude Code，手动** | `git clone https://github.com/senlindesign/proof.git`，再 `cp -R proof/skills/proof ~/.claude/skills/` |
| **Codex，手动** | `git clone https://github.com/senlindesign/proof.git`，再 `cp -R proof/skills/proof ~/.codex/skills/` |
| **Cursor、Windsurf 等** | 让 Agent 读 `skills/proof/SKILL.md` |

也可以把这段话直接发给能执行命令的 Agent：

```text
帮我安装 Proof 技能：克隆 https://github.com/senlindesign/proof，把里面的 skills/proof 文件夹复制到我的技能目录（Claude Code 是 ~/.claude/skills/，Codex 是 ~/.codex/skills/），然后确认 SKILL.md 在里面。
```

不用构建，没有依赖。如果装了 Python 3，它交付前还会检查每个页面。

## 怎么用

| 你想要 | 输入 |
| --- | --- |
| 马上要一个落地页 | `/proof landing` |
| 指定风格和深浅色 | `/proof pricing editorial dark` |
| 只要一个区块 | `/proof hero colorful` |
| 按你的用户来设计 | 补充四件事：谁会来，要让他们做什么，他们担心什么，你有哪些真实素材。也可以直接贴 PRD 或品牌规范。 |
| 用上你的品牌 | `/proof landing business — 主色 #E4572E，标题字体 Manrope` |
| 全部自己定 | `/proof blog editorial dark — 用 archetype B，不要订阅区块，做成这个项目里的 Next.js 页面` |
| 还没想好 | 只输入 `/proof`。它会问一轮问题，然后做出页面。 |

默认输出一个 HTML 文件。需要的话，它也可以按你项目的技术栈写代码。

---

## 适合 / 不适合

**适合：** 产品官网和营销页面；想要一份能直接上线的初稿；同一个产品想试几种风格。
**不适合：** App 内部界面和后台、电商网站、真实的表单提交、支付等业务逻辑。

## 常见问题

**要用 Mobbin 吗？** 不用。Mobbin 只是研究阶段的资料来源，所有知识都已经写进技能里，离线就能用。

**最后得到什么？** 默认是一个独立的 HTML 文件；你要的话，也可以是你项目技术栈的代码。

**页面里为什么有示例内容？** 为了让第一稿是完整的。它不会把编造的内容当成事实，QA 报告会列出每一处示例，方便替换。

**能用我自己的颜色和字体吗？** 能。给一个主色和一个标题字体就行，也可以直接贴品牌规范。

**怎么更新？** 重新运行安装命令，或者用 `/plugin update`，或者 `git pull` 后重新复制文件夹。

---

## 怎么做出来的

通过 [Mobbin](https://mobbin.com) 的 MCP 为真实产品页面写了 410 份研究记录，又研究了 55 个产品展示、32 个招牌手法和 72 条标题。另一个 agent 拿研究记录逐份核对知识文件。一套 19 个需求的黄金测试集覆盖所有页面类型、风格和深浅色，每个结果都要过脚本检查、编造内容核查和截图评审，详见 [`evals/`](evals/)。给贡献者的规则写在 [`AGENTS.md`](AGENTS.md)。

## 许可

[MIT](LICENSE)
