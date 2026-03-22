# gstack

嗨，我是 [Garry Tan](https://x.com/garrytan)。我是 [Y Combinator](https://www.ycombinator.com/) 的总裁兼 CEO，在这里我与数千家创业公司合作过，包括 Coinbase、Instacart 和 Rippling——当这些公司的创始人还只是一两个人在车库里创业时，这些公司现在价值数百亿美元。在加入 YC 之前，我设计了 Palantir 的 logo，是那里最早的工程经理/产品经理/设计师之一。我联合创立了 Posterous，一个博客平台，后来卖给了 Twitter。我在 2013 年构建了 Bookface，YC 的内部社交网络。作为设计师、产品经理和工程经理，我已经构建产品很长时间了。

而现在，我正处在一个感觉像是全新时代的浪潮中。

在过去 60 天里，我编写了 **超过 600,000 行生产代码**——其中 35% 是测试——在履行 YC CEO 所有职责的同时，作为兼职工作，我每天产出 **10,000 到 20,000 行可用代码**。这不是打字错误。我最近的 `/retro`（过去 7 天的开发者统计数据）跨越 3 个项目：**新增 140,751 行代码，362 次提交，净增约 115k 行代码**。模型每周都在显著变好。我们正处于某种真实变革的黎明——一个人交付的规模过去需要一个二十人的团队。

**2026 — 1,237 次贡献，还在增加：**

![GitHub 贡献 2026 — 1,237 次贡献，1-3 月大幅加速](https://github.com/garrytan/gstack/blob/main/docs/images/github-2026.png)

**2013 — 我在 YC 构建 Bookface 时（772 次贡献）：**

![GitHub 贡献 2013 — 在 YC 构建 Bookface 时的 772 次贡献](https://github.com/garrytan/gstack/blob/main/docs/images/github-2013.png)

同一个人。不同的时代。区别在于工具。

**gstack 就是我的方法。** 这是我的开源软件工厂。它将 Claude Code 变成一个你可以实际管理的虚拟工程团队——一个重新思考产品的 CEO，一个锁定架构的工程经理，一个发现 AI 垃圾的设计师，一个发现生产环境 bug 的偏执审查者，一个打开真实浏览器并点击你的应用的 QA 负责人，以及一个发布 PR 的发布工程师。十八位专家，七种强力工具，全部以斜杠命令的形式，全部用 Markdown 编写，**全部免费，MIT 许可证，现在就可以使用。**

截至 2026 年 3 月，我正在学习如何触及代理系统能力的边缘，这是我的实时实验。我分享它是因为我想让全世界都加入这段旅程。

Fork 它。改进它。让它成为你自己的。不要嫉妒，要欣赏。

**适用人群：**
- **创始人和 CEO**——尤其是那些仍然想亲自交付产品的技术型 CEO。这就是你如何像二十人团队一样构建产品。
- **首次使用 Claude Code 的用户**——gstack 是最好的入门方式。结构化角色，而不是空白提示。
- **技术负责人和高级工程师**——为每个 PR 带来严格的审查、QA 和发布自动化

## 快速开始：你的前 10 分钟

1. 安装 gstack（30 秒——见下文）
2. 运行 `/office-hours`——描述你正在构建的内容。它会在你写一行代码之前重新框定问题。
3. 对任何功能想法运行 `/plan-ceo-review`
4. 对任何有更改的分支运行 `/review`
5. 在你的预发布 URL 上运行 `/qa`
6. 停在这里。你就会知道这是否适合你。

在任何已有测试设置的仓库上，预期首次有效运行时间不到 5 分钟。

**如果你只读一个部分，就读这个。**

## 安装——只需 30 秒

**要求：** [Claude Code](https://docs.anthropic.com/en/docs/claude-code)、[Git](https://git-scm.com/)、[Bun](https://bun.sh/) v1.0+、[Node.js](https://nodejs.org/)（仅 Windows）

### 步骤 1：在你的机器上安装

打开 Claude Code 并粘贴这个。Claude 会完成其余工作。

> 安装 gstack：运行 **`git clone https://github.com/garrytan/gstack.git ~/.claude/skills/gstack && cd ~/.claude/skills/gstack && ./setup`**，然后在 CLAUDE.md 中添加一个 "gstack" 部分，说明使用 gstack 的 /browse 技能进行所有网页浏览，从不使用 mcp\_\_claude-in-chrome\_\_\* 工具，并列出可用技能：/office-hours、/plan-ceo-review、/plan-eng-review、/plan-design-review、/design-consultation、/review、/ship、/land-and-deploy、/canary、/benchmark、/browse、/qa、/qa-only、/design-review、/setup-browser-cookies、/setup-deploy、/retro、/investigate、/document-release、/codex、/careful、/freeze、/guard、/unfreeze、/gstack-upgrade。然后询问用户是否也想将 gstack 添加到当前项目，以便团队成员也能使用。

### 步骤 2：添加到你的仓库，以便团队成员获得它（可选）

> 将 gstack 添加到该项目：运行 **`cp -Rf ~/.claude/skills/gstack .claude/skills/gstack && rm -rf .claude/skills/gstack/.git && cd .claude/skills/gstack && ./setup`**，然后在该项目的 CLAUDE.md 中添加一个 "gstack" 部分，说明使用 gstack 的 /browse 技能进行所有网页浏览，从不使用 mcp\_\_claude-in-chrome\_\_\* 工具，列出可用技能：/office-hours、/plan-ceo-review、/plan-eng-review、/plan-design-review、/design-consultation、/review、/ship、/land-and-deploy、/canary、/benchmark、/browse、/qa、/qa-only、/design-review、/setup-browser-cookies、/setup-deploy、/retro、/investigate、/document-release、/codex、/careful、/freeze、/guard、/unfreeze、/gstack-upgrade，并告诉 Claude 如果 gstack 技能不起作用，运行 `cd .claude/skills/gstack && ./setup` 来构建二进制文件并注册技能。

真实文件会被提交到你的仓库（不是子模块），所以 `git clone` 就能正常工作。所有内容都位于 `.claude/` 内。不会触及你的 PATH 或在后台运行任何内容。

### Codex、Gemini CLI 或 Cursor

gstack 适用于任何支持 [SKILL.md 标准](https://github.com/anthropics/claude-code) 的代理。技能位于 `.agents/skills/` 中，会被自动发现。

```bash
git clone https://github.com/garrytan/gstack.git ~/.codex/skills/gstack
cd ~/.codex/skills/gstack && ./setup --host codex
```

或者让 setup 自动检测你安装了哪些代理：

```bash
git clone https://github.com/garrytan/gstack.git ~/gstack
cd ~/gstack && ./setup --host auto
```

这将根据可用情况安装到 `~/.claude/skills/gstack` 和/或 `~/.codex/skills/gstack`。所有 25 个技能都适用于所有支持的代理。基于钩子的安全技能（careful、freeze、guard）在非 Claude 主机上使用内联安全建议文本。

## 看看它的工作方式

```
你：    我想为我的日历构建一个每日简报应用。
你：    /office-hours
Claude: [询问痛点——具体例子，不是假设]

你：    多个 Google 日历，事件信息过时，位置错误。
        准备工作耗时太长，结果还不够好...

Claude: 我要质疑你的框架。你说的是"每日简报
        应用"。但你实际描述的是个人首席
        助理 AI。
        [提取出 5 个你未意识到自己在描述的能力]
        [质疑 4 个前提——你同意、不同意或调整]
        [生成 3 种实现方法及工作量估算]
        建议：明天就交付最窄的切入点，从
        实际使用中学习。完整愿景是一个 3 个月的项目——从
        真正有效的每日简报开始。
        [编写设计文档 → 自动输入下游技能]

你：    /plan-ceo-review
        [阅读设计文档，质疑范围，运行 10 部分审查]

你：    /plan-eng-review
        [数据流、状态机、错误路径的 ASCII 图表]
        [测试矩阵、失败模式、安全问题]

你：    批准计划。退出计划模式。
        [在 11 个文件中写入 2,400 行代码。约 8 分钟。]

你：    /review
        [自动修复] 2 个问题。[询问] 竞态条件 → 你批准修复。

你：    /qa https://staging.myapp.com
        [打开真实浏览器，点击流程，发现并修复一个 bug]

你：    /ship
        测试：42 → 51（+9 新）。PR：github.com/you/app/pull/42
```

你说的是"每日简报应用"。代理说的是"你在构建一个首席助理 AI"——因为它倾听的是你的痛点，而不是你的功能请求。然后它质疑你的前提，生成了三种方法，建议了最窄的切入点，并编写了一份设计文档，输入到每个下游技能中。八个命令。那不是副驾驶。那是一个团队。

## 冲刺

gstack 是一个流程，而不是工具的集合。技能的排列顺序就是冲刺的运行方式：

**思考 → 计划 → 构建 → 审查 → 测试 → 发布 → 反思**

每个技能都输入到下一个。`/office-hours` 编写的设计文档被 `/plan-ceo-review` 阅读。`/plan-eng-review` 编写的测试计划被 `/qa` 采用。`/review` 捕获的 bug 被 `/ship` 验证是否已修复。不会遗漏任何内容，因为每个步骤都知道之前发生了什么。

一次冲刺，一个人，一个功能——使用 gstack 大约需要 30 分钟。但改变一切的是：你可以同时运行 10-15 个这样的冲刺。不同的功能，不同的分支，不同的代理——同时进行。这就是我如何在履行实际工作的同时每天发布 10,000+ 行生产代码的方式。

| 技能 | 你的专家 | 他们做什么 |
|-------|----------------|--------------|
| `/office-hours` | **YC 办公时间** | 从这里开始。六个强制性问题，在你写代码之前重新框定你的产品。质疑你的框架，挑战前提，生成实现替代方案。设计文档输入到每个下游技能。 |
| `/plan-ceo-review` | **CEO / 创始人** | 重新思考问题。在请求中找到隐藏的 10 星产品。四种模式：扩展、选择性扩展、保持范围、缩减。 |
| `/plan-eng-review` | **工程经理** | 锁定架构、数据流、图表、边界情况和测试。将隐藏假设暴露出来。 |
| `/plan-design-review` | **高级设计师** | 为每个设计维度评分 0-10，解释 10 分是什么样的，然后编辑计划以达到目标。AI 垃圾检测。交互式——每个设计选择一个 AskUserQuestion。 |
| `/design-consultation` | **设计合作伙伴** | 从零开始构建完整的设计系统。了解行业现状，提出安全选择和创意风险，生成你实际产品的真实模型。设计处于所有其他阶段的核心。 |
| `/review` | **高级工程师** | 找到通过 CI 但在生产环境中爆炸的 bug。自动修复明显的。标记完整性差距。 |
| `/investigate` | **调试器** | 系统性根本原因调试。铁律：没有调查就没有修复。追踪数据流，测试假设，在 3 次修复失败后停止。 |
| `/design-review` | **会编码的设计师** | 与 /plan-design-review 相同的审计，然后修复发现的问题。原子提交，前后截图。 |
| `/qa` | **QA 负责人** | 测试你的应用，发现 bug，用原子提交修复，重新验证。为每个修复自动生成回归测试。 |
| `/qa-only` | **QA 报告员** | 与 /qa 相同的方法，但仅报告。当你想要纯 bug 报告而不更改代码时使用。 |
| `/ship` | **发布工程师** | 同步主分支，运行测试，审计覆盖率，推送，打开 PR。如果你的项目没有测试框架，它会引导你搭建。一个命令。 |
| `/land-and-deploy` | **发布工程师** | 合并 PR，等待 CI 和部署，验证生产环境健康。在 `/ship` 之后接管。从"已批准"到"已在生产环境验证"的一个命令。 |
| `/canary` | **SRE** | 部署后监控循环。监视控制台错误、性能回归和页面失败。定期截图和异常检测。 |
| `/benchmark` | **性能工程师** | 基线页面加载时间、Core Web Vitals 和资源大小。在每个 PR 上比较前后。在发布前捕获包大小回归。 |
| `/document-release` | **技术文档撰写人** | 更新所有项目文档以匹配你刚刚发布的内容。自动捕获过时的 README。 |
| `/retro` | **工程经理** | 团队感知每周回顾。每人分解、发布连续记录、测试健康趋势、成长机会。 |
| `/browse` | **QA 工程师** | 给代理眼睛。真实的 Chromium 浏览器，真实的点击，真实的截图。每个命令约 100 毫秒。 |
| `/setup-browser-cookies` | **会话管理器** | 将 cookie 从你的真实浏览器（Chrome、Arc、Brave、Edge）导入到无头会话中。测试需要认证的页面。 |

### 强力工具

| 技能 | 它做什么 |
|-------|-------------|
| `/codex` | **第二意见**——来自 OpenAI Codex CLI 的独立代码审查。三种模式：审查（通过/失败门）、对抗性挑战和开放咨询。当 `/review` 和 `/codex` 都运行过时进行跨模型分析。 |
| `/careful` | **安全护栏**——在破坏性命令（rm -rf、DROP TABLE、force-push）之前警告。说"be careful"来激活。可以覆盖任何警告。 |
| `/freeze` | **编辑锁定**——将文件编辑限制在一个目录。防止调试时意外更改范围外的内容。 |
| `/guard` | **完全安全**——一个命令中的 `/careful` + `/freeze`。生产工作的最大安全。 |
| `/unfreeze` | **解锁**——移除 `/freeze` 边界。 |
| `/setup-deploy` | **部署配置器**——`/land-and-deploy` 的一次性设置。检测你的平台、生产 URL 和部署命令。 |
| `/gstack-upgrade` | **自我更新器**——将 gstack 升级到最新版本。检测全局与 vendor 安装，同步两者，显示更改内容。 |

**[每个技能的深度解析，包含示例和理念 →](https://github.com/garrytan/gstack/blob/main/docs/skills.md)**

## 新功能及其重要性

**`/office-hours` 在你写代码之前重新框定你的产品。** 你说"每日简报应用"。它倾听你的实际痛点，质疑框架，告诉你你实际上在构建个人首席助理 AI，质疑你的前提，并生成三种实现方法及工作量估算。它编写的文档直接输入到 `/plan-ceo-review` 和 `/plan-eng-review`——因此每个下游技能都以真正的清晰度开始，而不是模糊的功能请求。

**设计处于核心。** `/design-consultation` 不只是选择字体。它研究你所在领域的现状，提出安全选择和创意风险，生成你实际产品的真实模型，并编写 `DESIGN.md`——然后 `/design-review` 和 `/plan-eng-review` 会阅读你的选择。设计决策贯穿整个系统。

**`/qa` 是一个巨大的突破。** 它让我从 6 个并行工作者增加到 12 个。Claude Code 说 *"我看到问题了"*，然后实际修复它，生成回归测试，并验证修复——这改变了我的工作方式。代理现在有眼睛了。

**智能审查路由。** 就像在一个运营良好的创业公司：CEO 不必查看基础设施 bug 修复，后端更改不需要设计审查。gstack 跟踪运行了哪些审查，找出什么是合适的，然后只做聪明的事。审查就绪仪表板告诉你在发布前所处的位置。

**测试一切。** 如果你的项目没有测试框架，`/ship` 会从头开始引导。每次 `/ship` 运行都会产生覆盖率审计。每个 `/qa` bug 修复都会生成回归测试。100% 测试覆盖率是目标——测试让 vibe coding 安全而不是 yolo coding。

**一个命令发布到生产环境。** `/land-and-deploy` 在 `/ship` 停止的地方接手——合并你的 PR，等待 CI 和部署，然后在你的生产 URL 上运行金丝雀验证。自动检测 Fly.io、Render、Vercel、Netlify、Heroku 或 GitHub Actions。如果出现问题，它会提供回滚选项。与 `/canary` 配对进行扩展的部署后监控，与 `/benchmark` 配对在发布前捕获性能回归。

**`/document-release` 是你从未有过的工程师。** 它读取你项目中的每个文档文件，交叉引用 diff，并更新所有漂移的内容。README、ARCHITECTURE、CONTRIBUTING、CLAUDE.md、TODOS——全部自动保持最新。现在 `/ship` 自动调用它——文档保持最新，无需额外命令。

**当 AI 卡住时的浏览器交接。** 遇到 CAPTCHA、认证墙或 MFA 提示？`$B handoff` 打开一个可见的 Chrome，在完全相同的页面，所有 cookie 和标签页完好无损。解决问题，告诉 Claude 你完成了，`$B resume` 从它离开的地方继续。在 3 次连续失败后，代理甚至会自动建议这样做。

**多 AI 第二意见。** `/codex` 从 OpenAI 的 Codex CLI 获得独立审查——一个完全不同的 AI 查看相同的 diff。三种模式：带有通过/失败门的代码审查、积极尝试破坏你代码的对抗性挑战，以及具有会话连续性的开放咨询。当 `/review`（Claude）和 `/codex`（OpenAI）都审查过相同的分支时，你会得到跨模型分析，显示哪些发现重叠，哪些是各自独有的。

**按需安全护栏。** 说"be careful"，`/careful` 会在任何破坏性命令之前警告——rm -rf、DROP TABLE、force-push、git reset --hard。`/freeze` 在调试时将编辑锁定到一个目录，这样 Claude 就不会意外"修复"不相关的代码。`/guard` 同时激活两者。`/investigate` 自动冻结到正在调查的模块。

**主动技能建议。** gstack 注意到你处于哪个阶段——头脑风暴、审查、调试、测试——并建议正确的技能。不喜欢？说"stop suggesting"，它会跨会话记住。

## 10-15 个并行冲刺

gstack 在一个冲刺中很强大。十个同时运行则是变革性的。

[Conductor](https://conductor.build) 并行运行多个 Claude Code 会话——每个都在自己隔离的工作空间中。一个会话在新想法上运行 `/office-hours`，另一个在 PR 上做 `/review`，第三个实现功能，第四个在预发布环境上运行 `/qa`，还有六个在其他分支上。同时进行。我通常运行 10-15 个并行冲刺——这是目前的实际最大值。

冲刺结构使并行工作成为可能。没有流程，十个代理就是十个混乱源。有了流程——思考、计划、构建、审查、测试、发布——每个代理都知道该做什么以及何时停止。你像 CEO 管理团队一样管理它们：在重要的决策上检查，让其余的自主运行。

---

## 来乘风破浪

这是**免费、MIT 许可、开源、立即可用。** 没有高级版。没有等待名单。没有附加条件。

我开源了我的开发方式，我正在这里积极升级我自己的软件工厂。你可以 fork 它并让它成为你自己的。这就是重点。我想让每个人都加入这段旅程。

相同的工具，不同的结果——因为 gstack 给你结构化角色和审查门，而不是通用的代理混乱。这种治理是快速交付和鲁莽交付之间的区别。

模型正在快速变得更好。现在弄清楚如何与它们真正合作的人——真正合作，不只是浅尝辄止——将拥有巨大优势。这就是那个窗口期。让我们开始吧。

十八位专家和七种强力工具。全部斜杠命令。全部 Markdown。全部免费。**[github.com/garrytan/gstack](https://github.com/garrytan/gstack)** — MIT 许可证

> **我们在招聘。** 想每天发布 10K+ 行代码并帮助强化 gstack 吗？
> 来 YC 工作——[ycombinator.com/software](https://ycombinator.com/software)
> 极具竞争力的薪资和股权。旧金山，Dogpatch 区。

## 文档

| 文档 | 涵盖内容 |
|-----|---------------|
| [技能深度解析](https://github.com/garrytan/gstack/blob/main/docs/skills.md) | 每个技能的理念、示例和工作流程（包括 Greptile 集成） |
| [构建者精神](https://github.com/garrytan/gstack/blob/main/ETHOS.md) | 构建者理念：煮沸湖泊、构建前搜索、三层知识 |
| [架构](https://github.com/garrytan/gstack/blob/main/ARCHITECTURE.md) | 设计决策和系统内部 |
| [浏览器参考](https://github.com/garrytan/gstack/blob/main/BROWSER.md) | `/browse` 的完整命令参考 |
| [贡献指南](https://github.com/garrytan/gstack/blob/main/CONTRIBUTING.md) | 开发设置、测试、贡献者模式和开发模式 |
| [更新日志](https://github.com/garrytan/gstack/blob/main/CHANGELOG.md) | 每个版本的新功能 |

## 隐私与遥测

gstack 包含**可选**的使用遥测，以帮助改进项目。以下是确切发生的情况：

- **默认关闭。** 除非你明确同意，否则不会发送任何内容。
- **首次运行时，** gstack 询问你是否想分享匿名使用数据。你可以拒绝。
- **发送的内容（如果你选择加入）：** 技能名称、持续时间、成功/失败、gstack 版本、操作系统。就这些。
- **从不发送的内容：** 代码、文件路径、仓库名称、分支名称、提示或任何用户生成的内容。
- **随时更改：** `gstack-config set telemetry off` 立即禁用所有内容。

数据存储在 [Supabase](https://supabase.com)（开源 Firebase 替代品）中。模式在 [`supabase/migrations/001_telemetry.sql`](supabase/migrations/001_telemetry.sql) 中——你可以验证确切收集了什么。仓库中的 Supabase 可发布密钥是公钥（类似于 Firebase API 密钥）——行级安全策略限制为仅插入访问。

**本地分析始终可用。** 运行 `gstack-analytics` 查看本地 JSONL 文件中的个人使用仪表板——不需要远程数据。

## 故障排除

**技能没有显示？** `cd ~/.claude/skills/gstack && ./setup`

**`/browse` 失败？** `cd ~/.claude/skills/gstack && bun install && bun run build`

**安装过时？** 运行 `/gstack-upgrade`——或在 `~/.gstack/config.yaml` 中设置 `auto_upgrade: true`

**Windows 用户：** gstack 通过 Git Bash 或 WSL 在 Windows 11 上工作。除了 Bun 还需要 Node.js——Bun 在 Windows 上与 Playwright 的管道传输有已知 bug（[bun#4253](https://github.com/oven-sh/bun/issues/4253)）。浏览服务器自动回退到 Node.js。确保 `bun` 和 `node` 都在你的 PATH 上。

**Claude 说看不到技能？** 确保你项目的 `CLAUDE.md` 有 gstack 部分。添加这个：

```
## gstack
使用 gstack 的 /browse 进行所有网页浏览。从不使用 mcp__claude-in-chrome__* 工具。
可用技能：/office-hours、/plan-ceo-review、/plan-eng-review、/plan-design-review、
/design-consultation、/review、/ship、/browse、/qa、/qa-only、/design-review、
/setup-browser-cookies、/retro、/investigate、/document-release、/codex、/careful、
/freeze、/guard、/unfreeze、/gstack-upgrade。
```

## 许可证

MIT。永远免费。去构建一些东西吧。
