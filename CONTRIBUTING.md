# Contributing · 投稿指南

This repo started with one creator's method (Mx-Shell's *Zombie Scavenger*).
The roadmap is to collect **more AI-shortfilm creators' methods** — structured
the same way, so they stack with the Skill. Contributions welcome.

> 这个仓库从一位创作者（Mx-Shell《丧尸清道夫》）的方法起步，路线图是收录
> **更多 AI 短片创作者的方法**，用同一套结构整理，能和 Skill 叠加使用。欢迎投稿。

---

## What we accept · 接受什么

- **A new creator's method** — a documented prompt workflow with a public, citable source (livestream / post / their own published docs).
- **A new template** — an IP-stripped, reusable skeleton under `templates/`.
- **Fixes** — broken links, typos, translation improvements, clearer wording.

> - **新创作者的方法** —— 有公开可引用来源（直播 / 帖子 / 本人公开文档）的提示词工作流。
> - **新模板** —— 放进 `templates/` 的去 IP 通用骨架。
> - **修正** —— 死链、错别字、翻译改进、表述更清楚。

## What we don't accept · 不接受什么

- Prompts copied from a creator **without a public source** or against their wishes.
- Raw copyrighted material (full livestream videos, scraped docs). Link to the source instead.
- IP-name-heavy prompts with no generalized version (they get blocked by Seedance anyway).

> - 没有公开来源、或违背作者意愿搬运的提示词。
> - 原始版权素材（完整直播视频、扒下来的文档）—— 请改为链接到来源。
> - 满是 IP 名又没有通用化版本的提示词（反正会被 Seedance 拦）。

---

## How to submit a new prompt · 如何投稿一条提示词

1. Fork the repo and add a file under `prompts/` (original prompt) or `templates/` (IP-stripped skeleton).
2. Follow the **5-stage structure** ([methodology](./methodology.md) · [方法论](./methodology.zh.md)).
3. Fill in the template below and put it at the top of your file.
4. Open a PR. Keep the source declaration honest — credit the original creator.

Copy this header into your new file · 把下面这段抄到你的新文件开头：

```markdown
---
title: {{prompt / work title}}
creator: {{original creator name or handle}}
source: {{public URL — livestream / post / doc}}
video_type: {{transformation | multi-shot narrative | atmospheric | weapon-charge | combat}}
duration: {{e.g. 15s single-shot}}
target_models: {{Seedance 2.0 | Sora | Kling | Jimeng | Veo}}
license: {{© original creator, archived for educational reference — or MIT if you authored it}}
---

<!-- Then the prompt itself, in the 5-stage structure. -->
```

> 1. Fork 仓库，在 `prompts/`（原始提示词）或 `templates/`（去 IP 骨架）下加文件。
> 2. 按 **5 段式结构** 写（见上方链接）。
> 3. 把上面的模板填好放到文件开头。
> 4. 提 PR。来源声明要诚实 —— 给原作者署名。

---

## Quick checklist · 提交前自检

- [ ] Source URL is public and citable · 来源 URL 公开可引用
- [ ] Original creator credited · 已给原作者署名
- [ ] Follows the 5-stage structure · 符合 5 段式结构
- [ ] No raw copyrighted files committed · 没有提交原始版权文件
- [ ] If IP names present, a generalized version is also provided · 有 IP 名则附通用版

Thanks for helping grow the library. · 感谢一起把这个库做大。
