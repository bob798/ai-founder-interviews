---
layout: default
title: "复用指南：如何下载字幕并做 AI 访谈深度分析（yt-dlp + 清洗 + 模板）"
description: "手把手复用流程：用 yt-dlp 下载 YouTube / B 站字幕、VTT/SRT 字幕清洗脚本、常见 ASR 纠错对照表，以及 9 大块深度分析模板，把 2-4 小时长访谈提炼成结构化笔记。"
---

# 复用指南：如何下载字幕并做一篇 AI 访谈深度分析

本页把本仓库的工作流抽成可复用的步骤：**找视频 → 下字幕 → 清洗 → 套模板写分析**。完整内部记录见 [PROGRESS.md](https://github.com/bob798/ai-founder-interviews/blob/main/PROGRESS.md)。

## 复用流程总览

1. **确定视频来源**——YouTube 还是 B 站。
2. **检查字幕可用性**——`yt-dlp --skip-download --list-subs <URL>`。
3. **下载字幕**——见下方命令。
4. **清洗字幕**——VTT/SRT → 带时间戳纯文本。
5. **套用 9 大块模板**——读一篇已有 `analysis.md` 作样板。
6. **写分析**——按受众价值排序观点，标注原话 vs 加工。

## 1. 下载 YouTube 字幕

```bash
yt-dlp --skip-download --write-auto-sub --write-sub \
  --sub-lang "zh-Hans,zh,zh-CN,en,en-US" --convert-subs vtt \
  "https://www.youtube.com/watch?v=VIDEO_ID" -o "vid_%(id)s.%(ext)s"
```

> 注意：部分播客频道（如张小珺 YouTube 频道）**关闭了字幕**，需改用 B 站源。

## 2. 下载 B 站字幕（需登录 cookies）

```bash
# 一次性导出 Chrome cookies 到文件
yt-dlp --cookies-from-browser chrome --cookies /tmp/bili_cookies.txt \
  --skip-download "https://www.bilibili.com/video/BVxxxxxxx/"

# 列出可用字幕（B 站播客通常有 ai-zh，部分有人工 zh-CN）
yt-dlp --cookies /tmp/bili_cookies.txt \
  --skip-download --list-subs "https://www.bilibili.com/video/BVxxxxxxx/"

# 下载 ai-zh 字幕
yt-dlp --cookies /tmp/bili_cookies.txt \
  --skip-download --write-sub --sub-lang ai-zh \
  "https://www.bilibili.com/video/BVxxxxxxx/" -o "bili_NAME_%(id)s.%(ext)s"
```

> B 站 SESSDATA 通常几个月有效，过期需重新导出 cookies。Cookies 文件含敏感信息，**切勿提交到仓库**（本项目已在 `.gitignore` 忽略 `*cookies*`）。

## 3. 清洗字幕（VTT/SRT → 带时间戳纯文本）

```python
import re

def clean_vtt(input_file, output_file):
    with open(input_file, encoding='utf-8') as f:
        lines = f.read().split('\n')
    blocks, current_ts = [], None
    for line in lines:
        line = line.strip()
        if not line or line.startswith(('WEBVTT', 'Kind:', 'Language:')):
            continue
        if '-->' in line:
            m = re.match(r'^(\d{2}:\d{2}:\d{2})\.\d+ -->', line)
            if m:
                current_ts = m.group(1)
            continue
        if current_ts:
            blocks.append((current_ts, line))
    # 去掉连续重复行（自动字幕常见）
    deduped, prev = [], ''
    for ts, text in blocks:
        if text != prev:
            deduped.append((ts, text)); prev = text
    with open(output_file, 'w', encoding='utf-8') as f:
        for ts, text in deduped:
            f.write(f"[{ts}] {text}\n")
```

## 4. 常见 ASR 字幕错误对照表

B 站 / 自动字幕在 AI 术语上经常识别错，写分析时按此纠正：

| 正确 | 常见错误识别 |
|------|------------|
| OpenCode | OpenCloud / open call / open clo |
| agentic | A 卷 / A 证 / IJTIC |
| ChatGPT | 拆 GPT / 全 GBT / HGBT |
| 智谱 | 质朴 / 知否 |
| 杨植麟 | 杨志玲 / 杨志林 |
| 罗福莉 | 罗福利 |
| OpenAI | open i / open ap / off er ap |
| Anthropic | an athropic |
| post-training | 铺设训 / 波士顿 |
| Adam (优化器) | ADAM |
| DeepSeek | DPCV3 |
| ChatGLM | 全 gm / chat gm |

## 5. 分析模板：9 大块结构

每篇分析按统一模板输出（样板见任意一篇 `analysis.md`）：

1. **视频信息块**——标题 / 频道 / 时长 / URL / 字幕规模
2. **I. 上帝视角**——对谈真实结构 + 核心张力 + 三组对位
3. **II. 12 个核心观点**——按对受众的实操价值排序
4. **III. 思想三层挖掘**——学科知识 / 5 个心智模型 / 底层哲学信念
5. **IV. 思想的内在张力**——3–5 组矛盾辨析
6. **V. 可复制 vs 不可复制**——✅ / ❌ / ⚠️ 三张表
7. **VI. 三种角色的可执行启示**——研究员 / 创业者 / 个人成长
8. **VII. 分析方法说明 + 局限性**
9. **附录：5 个最高密度瞬间**——带原话引用与时间戳

**质量要求**：综合分 ≥ 8/10（完整性 / 逻辑 / 受众价值）。
**设计原则**：不硬贴学派标签、区分原话 vs 分析者加工、失败案例 > 成功案例、清单可执行、客观声明局限性。

---

[← 返回首页](./index.html) · [全部分析](https://github.com/bob798/ai-founder-interviews)
