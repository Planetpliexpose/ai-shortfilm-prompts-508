# 跨仓库 Marketplace 整合建议

> 你（jnMetaCode）既然同时拥有 superpowers-zh / agency-agents-zh / ai-shortfilm-prompts 多个 plugin 仓库，可以考虑统一 marketplace 入口。
> 下面是 3 种整合方案，**选哪个由你定**。

---

## 方案 A：完全独立运营（最简单）

```
ai-shortfilm-prompts      ← 独立仓库 + 独立 marketplace.json
superpowers-zh            ← 独立仓库 + 独立 marketplace.json
agency-agents-zh          ← 独立仓库 + 独立 marketplace.json
```

**优点**：互不耦合，各自迭代
**缺点**：用户得手动找你每个仓库；星数也分散

**适合**：你不想做生态聚合的话，这是默认状态。

---

## 方案 B：把 shortfilm-prompt skill 拆出来塞进 superpowers-zh（最激进）

```
superpowers-zh/skills/
├── chinese-code-review/
├── chinese-commit-conventions/
├── ...
└── shortfilm-prompt/        ← 新增

ai-shortfilm-prompts/        ← 保留作为 "方法论 + 案例集" 仓库
                                （不再含 .claude/skills/）
```

**优点**：3.4k 星仓库直接获得 shortfilm 能力，**单 skill 曝光最大化**
**缺点**：
- superpowers-zh 的定位从"AI 编程"扩展为"AI 通用"—— 定位混乱
- 视频提示词 skill 在编程 skill 海洋里被埋没（你不会去 superpowers-zh 找视频 skill）
- 后续维护时要在两个仓库同步

**不推荐**：方向不一致，会拖累 superpowers-zh 的纯净度。

---

## 方案 C：用一个总 marketplace 仓库聚合（推荐 ⭐）

新建一个 `jnmetacode-marketplace`（或者直接用 GitHub Profile README 当入口），把所有 plugin 都列进 `marketplace.json`：

```json
{
  "name": "jnMetaCode-marketplace",
  "description": "AI 不止语 · 所有 plugin 入口",
  "owner": {
    "name": "jnMetaCode",
    "url": "https://github.com/jnMetaCode"
  },
  "plugins": [
    {
      "name": "superpowers-zh",
      "description": "AI 编程超能力中文增强版（20 skills）",
      "source": "https://github.com/jnMetaCode/superpowers-zh"
    },
    {
      "name": "agency-agents-zh",
      "description": "211 个 AI 专家角色",
      "source": "https://github.com/jnMetaCode/agency-agents-zh"
    },
    {
      "name": "ai-shortfilm-prompts",
      "description": "AI 短片提示词方法论 + Skill",
      "source": "https://github.com/jnMetaCode/ai-shortfilm-prompts"
    },
    {
      "name": "shellward",
      "description": "AI Agent 安全中间件",
      "source": "https://github.com/jnMetaCode/shellward"
    }
  ]
}
```

用户可以一行命令把所有 plugin 同时装上：

```bash
# 假设 Claude Code 未来支持 marketplace 引用
claude plugin add https://github.com/jnMetaCode/jnmetacode-marketplace
```

或者直接读 marketplace.json 知道你有哪些项目，然后选装。

**优点**：
- 矩阵效应：用户进一个仓库，看到你所有项目
- 各仓库独立迭代，定位不冲突
- 你的 GitHub Profile 看起来更系统化
- 适合做"AI 不止语" 品牌输出

**缺点**：多一个仓库要维护（但 marketplace.json 是静态文件，不需要频繁更新）

---

## 我的具体建议

**短期（开源前 1-2 周）**：方案 A，先把 ai-shortfilm-prompts 独立跑起来。

**中期（如果反响好）**：转方案 C，做个 `jnmetacode-marketplace` 入口仓库。

**理由**：
- 短期不要分心建总仓库，先验证 ai-shortfilm-prompts 单独能跑起来
- 等 star 数过 100 之后，做总入口收割流量
- agency-agents-zh 11.7k 星 + superpowers-zh 3.4k 星 = 你已经有矩阵基础，做 jnmetacode-marketplace 是顺势而为

---

## 现在你可以做的具体动作

1. **保持 ai-shortfilm-prompts 独立的 plugin.json / marketplace.json**（已经搞定）
2. **在 superpowers-zh 的 README 加一行**："姊妹项目：[ai-shortfilm-prompts](https://github.com/jnMetaCode/ai-shortfilm-prompts) - AI 视频提示词方向"
3. **在 agency-agents-zh 同样加一行**
4. **未来反响好了，再开 jnmetacode-marketplace**

我可以帮你起草 superpowers-zh / agency-agents-zh README 的修改 PR 文案 —— 但因为这两个仓库是你自己的，直接 push 就行，不用走 PR 流程。
