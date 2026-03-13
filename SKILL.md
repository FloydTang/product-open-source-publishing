---
name: product-open-source-publishing
description: |
  产品开源发布标准化流程。当九两确认"产品可以开源"后，执行完整的产品开源流程：
  1. 按格式写入产品库文档
  2. 同步到 GitHub bjjl-knowledge-base 仓库
  3. 按标准创建开源仓库并发布
  触发场景：九两说"这个可以开源"、"定稿了"、"记录一下"
---

# 产品开源发布标准化流程

> 适用于 Skill、工具、脚本等产品形态的开源发布

---

## 触发条件

当九两说以下任一话语时触发：
- "这个可以开源"
- "定稿了"
- "记录一下"
- "这个发布到 GitHub"

---

## 完整流程

### 阶段一：产品库文档更新

#### 1.1 确定产品信息

获取以下信息（如果九两未明确，从现有文件推断）：
- 产品名称
- 用途（一句话说明）
- 适用场景
- 技术栈
- 当前状态（开发中/已完成）

#### 1.2 写入产品库文档

位置：`knowledge-base/半斤九两品牌库/开源产品/产品库.md`

格式：
```markdown
## YYYY-MM-DD 产品名

- **用途**: xxx
- **场景**: xxx
- **仓库**: （待创建）
- **状态**: 🚧 开发中
- **技术栈**: xxx
- **发布日期**: YYYY-MM-DD
```

#### 1.3 推送到 GitHub

```bash
cd knowledge-base
git add -A
git commit -m "feat: 新增产品 - 产品名"
git push origin main
```

---

### 阶段二：创建开源仓库

#### 2.1 准备仓库内容

创建临时目录，复制以下文件：

| 文件 | 说明 | 来源 |
|------|------|------|
| README.md | 项目介绍文档 | 必填，参考 Memory Engine 标准 |
| requirements.txt | 依赖列表 | Python 项目必填 |
| SKILL.md | Skill 定义 | 如果是 Skill 项目 |
| .gitignore | Git 忽略 | 可选 |

#### 2.2 创建 GitHub 仓库

使用 GitHub API 创建：

```bash
curl -X POST https://api.github.com/user/repos \
  -H "Authorization: token ${GITHUB_TOKEN}" \
  -d '{"name":"仓库名","description":"描述","private":false}'
```

Token: `${GITHUB_TOKEN}`

#### 2.3 推送到远程

```bash
git remote add origin https://${GITHUB_TOKEN}@github.com/FloydTang/仓库名.git
git push -u origin main
```

---

### 阶段三：更新产品库

#### 3.1 更新仓库链接

编辑 `半斤九两品牌库/开源产品/产品库.md`：

```markdown
- **仓库**: https://github.com/FloydTang/仓库名
- **状态**: ✅ 已发布
```

#### 3.2 推送到 GitHub

```bash
git add -A
git commit -m "chore: 产品名 已开源发布"
git push origin main
```

---

## README.md 标准结构

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
```bash
git clone https://github.com/FloydTang/项目名.git
cd 项目名
pip install -r requirements.txt
```

## 📂 项目结构
- 文件/目录说明

## ⚙️ 配置参数

## 🤝 贡献

## 📄 许可证

## 📞 联系

---

**Version**: x.x  
**Last Updated**: YYYY-MM-DD
```

---

## 注意事项

1. **必须先确认**：只有九两明确说"可以开源"才执行
2. **文档优先**：先更新产品库，再创建开源仓库
3. **标准格式**：README 必须包含特性、价值、快速开始、项目结构
4. **仓库命名**：
   - Skill：使用 skill 名称（kebab-case）
   - 工具：使用工具名称（kebab-case）
5. **Token 保密**：GitHub Token 不得泄露给外部

---

## 完整检查清单

- [ ] 确认九两说"可以开源"
- [ ] 产品写入产品库文档
- [ ] 产品库推送到 GitHub
- [ ] 创建开源仓库
- [ ] README.md 符合标准
- [ ] requirements.txt 存在（如适用）
- [ ] 代码推送到开源仓库
- [ ] 更新产品库状态为"已发布"
- [ ] 产品库推送到 GitHub

---

*标准化流程 | 版本 1.0 | 2026-03-13*
