# product-open-source-publishing 📦⚡

> 产品开源发布标准化流程 - 半斤九两科技

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**product-open-source-publishing** 是半斤九两科技自主研发的产品开源发布标准化流程 Skill，实现从产品确认到开源发布的全流程自动化。

---

## ✨ 特性

| 特性 | 说明 |
|------|------|
| **触发检测** | 自动识别九两的"可以开源"指令 |
| **标准化流程** | 产品库 → GitHub → 开源仓库 → 更新状态 |
| **一键发布** | 全流程自动化，减少人工操作 |
| **质量保证** | README 标准检查、依赖检查 |

---

## 🎯 价值与意义

### 解决什么问题？

**传统开源发布的痛点**：
- 流程分散，容易遗漏步骤
- 文档格式不统一
- 手动操作繁琐易出错

**product-open-source-publishing 的答案**：
- 标准化流程，确保不遗漏任何步骤
- 文档格式统一，质量有保证
- 自动化程度高，人工只需确认

### 适用场景

- 📦 Skill 开源发布
- 🛠️ 工具/脚本开源发布
- 📚 文档/知识库开源发布

---

## 🚀 快速开始

### 1. 触发条件

当九两说以下任一话语时自动触发：
- "这个可以开源"
- "定稿了"
- "记录一下"
- "这个发布到 GitHub"

### 2. 执行流程

```
阶段一：产品库文档更新
  ├── 确定产品信息
  ├── 写入产品库文档
  └── 推送到 GitHub

阶段二：创建开源仓库
  ├── 准备仓库内容（README.md 必填）
  ├── 创建 GitHub 仓库
  └── 推送到远程

阶段三：更新产品库
  ├── 更新仓库链接
  └── 推送到 GitHub
```

---

## 📂 项目结构

```
product-open-source-publishing/
├── SKILL.md           # Skill 定义文档（核心）
└── README.md         # 本文档
```

---

## 📋 检查清单

- [ ] 确认九两说"可以开源"
- [ ] 产品写入产品库文档
- [ ] 产品库推送到 GitHub
- [ ] 创建开源仓库
- [ ] **README.md 符合标准** ← 重点检查
- [ ] requirements.txt 存在（如适用）
- [ ] 代码推送到开源仓库
- [ ] 更新产品库状态为"已发布"
- [ ] 产品库推送到 GitHub

---

## 📝 README.md 标准结构

```markdown
# 项目名 📝⚡

> 项目一句话描述

## ✨ 特性
- 特性1
- 特性2

## 🎯 价值与意义
- 解决什么问题
- 适用场景

## 🚀 快速开始
- 克隆
- 安装依赖
- 配置
- 运行

## 📂 项目结构
- 目录结构说明

## ⚙️ 配置参数

## 🤝 贡献

## 📄 许可证

## 📞 联系
```

---

## ⚠️ 重要提醒

**每次开源发布前，必须检查 README.md 是否存在且符合标准！**

---

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

---

## 📄 许可证

MIT License

---

## 📞 联系

- 项目维护：[@FloydTang](https://github.com/FloydTang)
- 作者：Mars (半斤九两科技)

---

**Version**: 1.0  
**Last Updated**: 2026-03-13

---

<!-- jiuliang-about-start -->

## 关于半斤九两 / About EVEN BETTER

半斤九两科技（EVEN BETTER）专注“外贸 + AI”的真实落地。我们希望帮助外贸企业把产品、客户、渠道和团队流程，沉淀成客户看得懂、渠道跑得动、团队留得下的系统。

我们主要提供：

- 外贸 AI 落地方法：围绕 Build / Traffic / Team，判断企业该先建资产、放流量，还是建系统。
- 企业表达与内容增长：把产品、案例、FAQ、老板经验和信任证据，整理成海外客户看得懂的内容资产。
- 主动开发流程：从客户画像、线索搜索、客户背调到开发信和跟进复盘，跑出可复用闭环。
- 团队 AI 工作流：把经验写进 AGENTS.md、SOP、模板库、检查清单和可复用 Skill。

更多内容可以查看我们整理的 [《外贸人 Codex 蓝皮书》](https://github.com/FloydTang/waimaoren-codex-bluebook)。

### 找到我们

- 官网：[tang92.com](https://tang92.com)
- 公众号：半斤九两
- GitHub：[@FloydTang](https://github.com/FloydTang)

扫码关注公众号，领取后续模板、案例和更新；也可以通过公众号后台留言联系九两。

<p>
  <img src="https://raw.githubusercontent.com/FloydTang/waimaoren-codex-bluebook/main/assets/wechat-qr.png" alt="半斤九两公众号二维码" width="180">
</p>

<!-- jiuliang-about-end -->
