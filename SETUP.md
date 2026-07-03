# 🚀 如何启用 · Setup Guide

## 1) 创建「特殊仓库」 · Create the magic repo
GitHub 个人主页的 overview 来自一个 **与用户名同名** 的仓库。

- 新建仓库,名称必须是 **`Horace-Maxwell`**(和你的用户名一字不差)
- 设为 **Public**
- 建好后它的 README 就会显示在你主页顶部

## 2) 放入文件 · Add the files
把本文件夹的内容复制进该仓库根目录:

```
Horace-Maxwell/
├── README.md
├── assets/
│   └── banner.svg
└── .github/
    └── workflows/
        └── snake.yml   (可选)
```

命令行方式:

```bash
git clone https://github.com/Horace-Maxwell/Horace-Maxwell.git
cd Horace-Maxwell
# 把 README.md、assets/、.github/ 复制进来
git add .
git commit -m "✨ cosmic profile · 观天执天"
git push
```

## 3) 贡献蛇动画 · Contribution snake ✅ 已启用
`.github/workflows/snake.yml` 已运行,蛇图已接入 `README.md`,之后每 12 小时自动刷新。
以下为手动搭建步骤(供参考 / 迁移时用):
1. 到仓库 **Actions** 页,运行一次 **generate snake**(workflow_dispatch)。
2. 运行成功后会生成 `output` 分支,在 README 里引用:

```html
<img src="https://raw.githubusercontent.com/Horace-Maxwell/Horace-Maxwell/output/snake-dark.svg" width="100%" />
```

## 说明 · Notes
- 所有数据卡片(followers / 语言占比 / streak / 奖杯 / 贡献星轨)都会**自动读取你的真实数据**,无需手填。
- 配色为「深空紫 · 星金 · 天青」,深色 / 浅色模式都清晰可读。
- `banner.svg` 是纯手写 SVG,内置**星空闪烁、流星划过、罗盘八卦旋转**动画,GitHub 原生支持,无需任何服务。
- 想改标语 / 颜色 / 术数标签,直接编辑 `README.md` 与 `assets/banner.svg` 即可。
