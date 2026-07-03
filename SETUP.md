# 🚀 说明 · How this profile works

个人主页 overview 来自与用户名同名的仓库 **`Horace-Maxwell/Horace-Maxwell`**(已建好并上线)。
本设计的核心原则:**不依赖任何会限流/掉线的第三方实时服务**,能挂的一律换成
「GitHub Actions 生成静态 SVG 提交进仓库」或已验证长期可靠的服务。

## 🧩 组成 · Components

| 区块 | 方案 | 可靠性 |
|---|---|---|
| 顶部 banner | 手写动画 SVG [`assets/banner.svg`](assets/banner.svg) | ⭐ 提交式,永不挂 |
| 动态标语 | 手写动画 SVG [`assets/typing.svg`](assets/typing.svg) | ⭐ 提交式 |
| 访问量 / 粉丝 / 标签 | komarev · shields.io | ✅ 已验证 |
| 术数 / 技术栈徽章 | shields.io | ✅ 已验证 |
| 代表作卡片 | shields.io(实时 star/fork/语言) | ✅ 已验证 |
| 统计 / 语言 / 编码时段 | **`github-profile-summary-cards`** Action → [`assets/cards/`](assets/cards) (tokyonight 主题) | ⭐ 提交式,真实聚合数据 |
| 连续贡献 streak | streak-stats.demolab.com | ✅ 已验证 |
| 贡献蛇 | **`Platane/snk`** Action → `output` 分支 | ⭐ 提交式 |
| 页脚 | 手写 SVG [`assets/footer.svg`](assets/footer.svg) | ⭐ 提交式 |

> ❌ 已弃用:github-readme-stats、github-readme-activity-graph、readme-typing-svg、
> github-profile-trophy、capsule-render —— 这些 vercel 公共实例经常限流,就是之前满屏「?」的元凶。

## ⚙️ 自动化 · Workflows

- [`.github/workflows/profile-cards.yml`](.github/workflows/profile-cards.yml) —— 每天生成
  tokyonight 统计卡到 `assets/cards/`(只保留一套主题,不污染仓库)。用内置 `GITHUB_TOKEN`,无需 PAT。
- [`.github/workflows/snake.yml`](.github/workflows/snake.yml) —— 每 12 小时生成贪吃蛇到 `output` 分支。

两者都可在仓库 **Actions** 页手动 `Run workflow` 立即刷新。

## 🎨 想改 · Customize

- 换统计卡配色:把 `profile-cards.yml` 里 workflow 复制的 `tokyonight` 换成其它主题名
  (如 `shades_of_purple`、`radical`、`synthwave`、`midnight_purple`),同时改 README 里 `assets/cards/` 引用即可。
- 改标语 / 术数标签 / 配色:直接编辑对应的 `assets/*.svg` 与 `README.md`。
- 本地副本在 `Downloads/github-profile/`。
