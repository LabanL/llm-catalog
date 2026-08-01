# 🤖 2026 大模型 API 清单

实时对比 13 家厂商、40+ 主流大模型的 API 定价、上下文窗口、多模态能力与综合评分。

本仓库包含两份数据清单：
- **[`index.html`](./index.html)** — 文本大模型（对话/推理/代码）：13 家厂商，40+ 模型
- **[`media.html`](./media.html)** — 音视频大模型（视频/图像/TTS/ASR/音乐）：13 家厂商，30+ 模型

🔗 **在线访问**：https://labanl.github.io/llm-catalog/

## 📋 包含字段

### 文本模型 (index.html)

| 字段 | 说明 |
|------|------|
| 模型厂商 | OpenAI / Anthropic / Google / DeepSeek / 豆包 / 通义千问 / 智谱AI / MiniMax / 月之暗面 / 小米 / 腾讯混元 / xAI / 美团 |
| 模型名称 | 含版本号 |
| 模型参数量 | 已公开的标注 |
| 最大输入 | 上下文窗口长度 |
| 最大输出 | 单次输出 token 上限 |
| 输入价格 | 每百万 token |
| 缓存命中价格 | Prompt Cache 折扣价 |
| 输出价格 | 每百万 token |
| 多模态 | 支持的输入类型（文本/图片/音频/视频） |
| 评分 | Artificial Analysis Coding Index（2026年6月） |
| 官网地址 | 各厂商官方定价页面 |

### 音视频模型 (media.html)

| 字段 | 说明 |
|------|------|
| 模型厂商 | OpenAI / Google / 豆包 / 通义千问 / 智谱AI / MiniMax / xAI / 腾讯混元 / 美团（Anthropic / DeepSeek / Kimi / MiMo 暂未提供相应 API） |
| 模型名称 | 含版本号 |
| 类型 | 🎥 视频 / 🖼️ 图像 / 🔊 TTS/ASR / 🎵 音乐 |
| 关键能力 | 模型特性描述 |
| 输入规格 | 支持的输入模态与限制 |
| 输出规格 | 分辨率、时长、采样率等 |
| 价格 | 按官方原币种 / 美元计费（视频多按秒、图片按张、音频按时长） |
| 官网地址 | 各厂商官方 API 文档 |

## ✨ 功能特性

- 🔍 实时搜索：按模型名或厂商筛选
- 🏷️ 快捷筛选：全部 / 国产 / 海外 / 极致低价 / 旗舰
- ↕️ 列排序：点击表头按价格、评分、上下文等排序
- 💡 价格高亮：绿色=低价、橙色=中等、红色=高价
- 📱 响应式布局：移动端可横向滚动

## 📊 数据来源

- 定价数据：各厂商官方定价页面
- 评分数据：[Artificial Analysis](https://artificialanalysis.ai/) Coding Index（2026年6月）
- 多模态能力：各厂商官方文档

## 🗓️ 更新记录

- **2026-07-31**：
  - 移除 MiniMax H3（视频生成模型从文本模型清单移至独立音视频页面）
  - 新增音视频模型清单页面 [`media.html`](./media.html)：覆盖 9 家厂商 30+ 模型，包含视频生成（OpenAI Sora 2 / Google Veo 3.1 / Doubao Seedance 2.0 / Wan2.7 / CogVideoX / Hailuo-03 / 混元生视频）、图像生成（GPT-Image-2 / Imagen 4 / Nano Banana 2 / Seedream 3.0 / CogView-3 / HY Image 3.0）、TTS/ASR（GPT-Realtime-1.5 / Qwen3-TTS-ASR / Doubao 语音 / GLM-4-Voice / Speech-02 / 混元 TTS/ASR）、音乐生成（Lyria 3 / Music-01）
  - 新增 xAI Grok 4.5 文本模型，新增 Grok Voice Think Fast 2.0 与 Grok Imagine Video 1.5 音视频模型
  - 顶部增加页面间导航：文本模型 ↔ 音视频模型
  - 豆包模型调整为 5 款（对齐火山方舟模型广场「深度思考」首推）：保留 Doubao Seed 2.1 Pro / 2.1 Turbo，新增 Seed Evolving（1M 上下文，¥6/¥30 旗舰价）、Seed 2.0 Lite（豆包首款全模态理解模型，¥0.6/¥3.6）、Seed 2.0 Mini（低时延低成本，¥0.2/¥2）
  - 移除豆包 4 款已下线/降级模型：Seed 2.0 Code、1.6 系列等往期模型
- **2026-07-27**：新增腾讯混元 Hy3（295B MoE，192K 输入，¥1/¥4 定价，Apache 2.0 开源）；新增 Kimi K3（2.8T MoE，1M 上下文，¥20/¥100 定价），移除 Kimi K2.5；更新 Gemini 系列：新增 3.6 Flash / 3.5 Flash-Lite，修正 3.1 Pro / 3.5 Flash 价格
- **2026-07-15**：更新 Anthropic 与 OpenAI 新模型
  - 新增 Claude Fable 5（Mythos 级旗舰，1M 上下文，128K 输出）
  - 新增 Claude Sonnet 5（新默认模型，1M 上下文）
  - 新增 GPT-5.6 Sol / Terra / Luna 三档模型
- **2026-06-29**：初始版本，覆盖 10 家厂商 30+ 模型
  - 新增「多模态」和「评分」两列
  - 补充小米 MiMo V2.5 / V2.5 Pro、豆包 Seed 2.1、GLM-5.2、Kimi K2.7 Code

## 📄 License

MIT
