# AI 创始人 & 研究员深度访谈分析 | AI Founder & Researcher Interview Analyses

> 对中文互联网最有价值的 **AI 创始人、AI 研究员长访谈**（张小珺商业访谈录、WhynotTV、雪球《方略》等）做的**结构化深度拆解**。
> 每篇分析 = 1 场 2–4 小时对谈 → 8000–9000 字 / 9 大块结构（上帝视角 · 12 个核心观点 · 思想三层挖掘 · 内在张力 · 可复制清单 · 三角色启示）。

**关键词 / Keywords**：AI 创始人访谈、大模型创业、AI 研究方法论、张小珺商业访谈录解读、段永平投资、杨植麟 Kimi、罗福莉 小米大模型、何小鹏 小鹏汽车、张鹏 智谱 AI、姚顺宇 DeepMind/Anthropic、翁家翌 OpenAI、Scaling Law、强化学习 RL、Post-training、Agent、Multi-agent、机会成本、长期主义。

---

## 📑 目录 Table of Contents

- [这是什么 What is this](#这是什么-what-is-this)
- [访谈分析索引 Index](#访谈分析索引-index)
- [逐篇精华 Highlights](#逐篇精华-highlights)
- [分析方法 Methodology](#分析方法-methodology)
- [如何复用 How to reproduce](#如何复用-how-to-reproduce)
- [常见问题 FAQ](#常见问题-faq)
- [免责声明 Disclaimer](#免责声明-disclaimer)

---

## 这是什么 What is this

这是一个开源的 **AI 行业长访谈深度分析库**。我们挑选高信息密度的创始人 / 研究员对谈视频，下载并清洗字幕，然后用一套固定的 **5 轮 Self-Debate** 流程，把 2–4 小时口语对话提炼为可检索、可执行的结构化笔记。

适合人群：

- **AI 研究员 / 工程师** —— 看一线从业者怎么谈 Scaling Law、RL、post-training、Agent、Infra
- **创业者 / CEO** —— 看创始人怎么做范式判断、组织管理、商业化取舍
- **投资人 / 行业研究者** —— 一篇笔记抵一次 3 小时播客，带原话时间戳可回溯
- **个人成长读者** —— 提炼"可复制 vs 不可复制"的方法论清单

目前已收录 **7 篇深度分析**，覆盖大模型、自动驾驶、机器人、AI 投资等方向。

---

## 访谈分析索引 Index

| # | 嘉宾 Guest | 身份 / 公司 | 主持 · 频道 | 时长 | 核心议题 | 分析 |
|---|-----------|------------|------------|------|---------|------|
| 1 | **段永平** | 投资人 · OPPO/vivo/步步高 | 方三文 · 雪球《方略》 | 1:53 | 机会成本、不为清单、长期主义、企业文化 | [📄 阅读](./duan-yongping-fang-sanwen-2025/analysis.md) · [v2 带时间戳](./duan-yongping-fang-sanwen-2025/analysis-v2.md) |
| 2 | **姚顺宇** | 研究员 · Google DeepMind / Anthropic | 张小珺 | 3:48 | 英雄主义终结、先跑实验、Scaling Law、长任务 | [📄 阅读](./yao-shunyu-zhang-xiaojun-en/analysis.md) |
| 3 | **翁家翌** | Infra 工程师 · OpenAI | WhynotTV Podcast #4 | 2:02 | 卖铲子、Infra 杠杆、自定义 reward、强化学习 | [📄 阅读](./weng-jiayi-whynottv-4/analysis.md) |
| 4 | **何小鹏** | 创始人 · 小鹏汽车 | 张小珺 #143 | 1:28 | 物理 AI vs 数字 AI、人形机器人、范式迭代 | [📄 阅读](./he-xiaopeng-zhang-xiaojun-2025/analysis.md) |
| 5 | **杨植麟** | 创始人 · Kimi / 月之暗面 | 张小珺 #113 | 1:41 | K2、Muon 优化器、Agentic LLM、模型即产品 | [📄 阅读](./yangzhilin-kimi-zhang-xiaojun-2025/analysis.md) |
| 6 | **罗福莉** | 大模型负责人 · 小米（前 DeepSeek） | 张小珺 #138 | 3:36 | OpenCode、群体智能、Agent 范式、卡资源分配 | [📄 阅读](./luofuli-zhang-xiaojun-2025/analysis.md) |
| 7 | **张鹏** | CEO · 智谱 AI | 张小珺 #129 | 2:26 | 清华血脉、政策窗口、百模大战、L0/L1/L2 分层 | [📄 阅读](./zhangpeng-zhipu-zhang-xiaojun-2025/analysis.md) |

> 进度、待处理视频与字幕抓取技术细节见 [PROGRESS.md](./PROGRESS.md)。

---

## 逐篇精华 Highlights

每篇的完整版含 12 个核心观点、三层思想挖掘、内在张力、可复制清单与原话时间戳。以下为入口摘要。

### 1. 段永平 × 方三文：一场"非典型成功者"的自我祛魅
> 减法主义、边界感、内驱、机会成本。
- **机会成本是投资唯一标尺**——"卖了茅台钱放哪？回答不了，讨论投资都是瞎扯。"
- **"做对的事"重于"把事情做对"**——5 秒判断是非省一辈子。
- **不为清单（Stop-doing List）**——30 年复利来自减法，不是加法。
- 👉 [完整分析](./duan-yongping-fang-sanwen-2025/analysis.md)

### 2. 姚顺宇 × 张小珺：一场"英雄主义终结"的解构对话
> 系统压倒个体、实验优先、Scaling Law 未死。
- **靠谱比聪明重要**——AI 行业最核心的特质不是天才，是对工作负责。
- **先跑实验，不信纯理论**——高能物理训练移植到 AI 研究。
- **Scaling Law 还没死**——大多数"天花板"都是实验 bug。
- 👉 [完整分析](./yao-shunyu-zhang-xiaojun-en/analysis.md)

### 3. 翁家翌 × WhynotTV：一个"铲子制造者"的自我解码
> 卖铲子比挖金、自定义评价体系、Infra 即杠杆。
- **找到卖铲子的位置，比挖金更重要**。
- **idea 非常便宜，验证 idea 的基础设施才值钱**。
- **对自己定义评价体系，但不能成为它的奴隶**。
- 👉 [完整分析](./weng-jiayi-whynottv-4/analysis.md)

### 4. 何小鹏 × 张小珺：一场"物理世界赌徒"的自我辩护
> 物理 AI ≠ 数字 AI、两成胜率、范式迭代。
- **早下注 > 敢下注**——判断力到位后，拖延本身就是风险。
- **物理世界和数字世界是两种维度，不是同一谱系的不同段位**。
- **"缝合怪"自我诊断法**——软件方法论 + AI 工具 ≠ AI 原生产品。
- 👉 [完整分析](./he-xiaopeng-zhang-xiaojun-2025/analysis.md)

### 5. 杨植麟（Kimi）× 张小珺：用爬山隐喻包装的技术战略告白
> 模型即产品、test-time scaling 双维度、用 RL 管团队。
- **"问题不可避免，问题可以解决"**（引自 David Deutsch）。
- **K2 关键创新**——Muon 优化器（替代 Adam，token efficiency ~2×）+ 大规模 MoE + 数据改写。
- **Agent 当前最大瓶颈 = 泛化性**。
- 👉 [完整分析](./yangzhilin-kimi-zhang-xiaojun-2025/analysis.md)

### 6. 罗福莉（小米大模型）× 张小珺：被 OpenCode 点燃的认知革命
> 群体智能、Agent 是协调层、去 DAU 叙事。
- **Agent 框架是弥补模型行动缺陷的协调层**——不是 UI，不是模型，是中间层。
- **训模型 ≈ 管团队**——群体智能 >> 个人英雄主义。
- **现在卡在卡上，不卡在 idea 上**——瓶颈是 GPU 验证速度。
- 👉 [完整分析](./luofuli-zhang-xiaojun-2025/analysis.md)

### 7. 张鹏（智谱 AI CEO）× 张小珺：一场"第一个吃螃蟹者"的复盘
> 政策窗口、百模大战、L0/L1/L2 分层、实用主义工程师。
- **科技成果转化 = 政策窗口 × 团队准备**。
- **百模大战焦虑：不是焦虑自己输，是焦虑市场塌掉**。
- **开源是品牌策略而非纯技术信仰**（GLM-130B / ChatGLM-6B）。
- 👉 [完整分析](./zhangpeng-zhipu-zhang-xiaojun-2025/analysis.md)

---

## 分析方法 Methodology

每篇分析遵循统一模板（详见 [PROGRESS.md](./PROGRESS.md)），输出 **9 大块结构**：

1. **视频信息块**——标题 / 频道 / 时长 / URL / 字幕规模
2. **I. 上帝视角**——对谈真实结构 + 核心张力 + 三组对位
3. **II. 12 个核心观点**——按对受众的实操价值排序
4. **III. 思想三层挖掘**——学科知识 / 5 个心智模型 / 底层哲学信念
5. **IV. 思想的内在张力**——3–5 组矛盾辨析
6. **V. 可复制 vs 不可复制**——✅ / ❌ / ⚠️ 三张表
7. **VI. 三种角色的可执行启示**——研究员 / 创业者 / 个人成长
8. **VII. 分析方法说明 + 局限性**
9. **附录：5 个最高密度瞬间**——带原话引用与时间戳

**质量要求**：综合分 ≥ 8/10（完整性 / 逻辑 / 受众价值三维度）。
**设计原则**：不硬贴学派标签、区分"原话 vs 分析者加工"、失败案例 > 成功案例、清单可执行、客观声明局限性。

---

## 如何复用 How to reproduce

> 📖 在线复用指南（含命令与脚本）：**[guide / 如何下载字幕并做 AI 访谈深度分析](https://bob798.github.io/ai-founder-interviews/guide.html)**

想用同一流程分析新视频？流程如下（完整脚本见 [PROGRESS.md](./PROGRESS.md#关键技术细节复用时直接看这部分)）：

1. **确定来源**——YouTube 还是 B 站
2. **检查字幕**——`yt-dlp --skip-download --list-subs URL`
3. **下载字幕**——YouTube 自动字幕 / B 站 `ai-zh`（需登录 cookies）
4. **清洗字幕**——VTT/SRT → 带时间戳纯文本（含 Python 脚本）
5. **读模板**——`duan-yongping-fang-sanwen-2025/analysis.md`
6. **写分析**——9 大块结构 + 附录
7. **更新进度**——回填 PROGRESS.md

PROGRESS.md 还附带 **B 站 / 张小珺频道常见 ASR 字幕错误对照表**（如 "OpenCode"→"OpenCloud"、"agentic"→"A 卷"），写分析时可直接参考纠错。

---

## 常见问题 FAQ

**Q：这些分析是 AI 生成的吗？**
是用结构化的多轮 Self-Debate 流程从原始字幕提炼的。原话引用带时间戳，可回原视频核对；分析者加工部分有明确标注。

**Q：和直接看播客 / 听原片有什么区别？**
一篇 8000 字笔记 ≈ 一场 2–4 小时对谈的可检索版本，按观点价值排序，并额外给出"可复制 vs 不可复制"的执行清单，省去反复拖进度条。

**Q：会继续更新吗？**
会。待处理视频与候选清单见 [PROGRESS.md](./PROGRESS.md)，欢迎 Issue / PR 提名值得分析的访谈。

**Q：可以转载吗？**
分析内容遵循下方免责声明，转载请注明出处并保留原视频链接。

---

## 免责声明 Disclaimer

- 本仓库为**第三方学习笔记**，与各访谈嘉宾、主持人、频道（张小珺、WhynotTV、雪球等）无任何关联。
- 所有观点均为对**公开访谈视频**的二次整理，可能存在**字幕 ASR 错误**与**整理者理解偏差**（二阶失真）。请以原视频为准。
- 版权归原视频作者所有，本仓库仅提供分析与索引，不包含完整字幕转录。
- 内容仅供学习研究，不构成任何投资 / 商业建议。

---

## 网站与 AI 适配 Site & AI-readiness

- 🌐 **在线站点（GitHub Pages）**：https://bob798.github.io/ai-founder-interviews/
- 已做 **SEO / GEO / AEO / AIO** 优化：每页独立 `<title>` 与 meta description、`sitemap.xml`、Schema.org 结构化数据（`Article` / `FAQPage` / `ItemList` / `BreadcrumbList`）、面向生成式引擎的 [`llms.txt`](https://bob798.github.io/ai-founder-interviews/llms.txt) 与 `robots.txt`（显式放行 GPTBot / ClaudeBot / PerplexityBot / Google-Extended 等）。

## 许可 License

分析笔记（本仓库原创文本）采用 **[CC BY-NC-SA 4.0](./LICENSE)**（署名 · 非商业 · 相同方式共享）。原视频版权归各自作者所有，本许可不覆盖原视频 / 字幕。

---

> ⭐ 如果这些分析对你有帮助，欢迎 Star 收藏。新访谈提名 / 纠错请提 [Issue](../../issues)。
