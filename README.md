# 🤖 2026 大模型 API 清单

实时对比 16 家厂商、48 款主流大模型的 API 定价、上下文窗口、多模态能力与综合评分。

本仓库包含三份数据清单：
- **[`index.html`](./index.html)** — 文本大模型（对话/推理/代码）：16 家厂商，48 款模型
- **[`media.html`](./media.html)** — 音视频大模型（视频/图像/TTS/ASR/音乐）：13 家厂商，44 款模型
- **[`open-source.html`](./open-source.html)** — 主流开源大模型（开放权重/可私有化部署）：27 家组织，61 款模型

🔗 **在线访问**：https://labanl.github.io/llm-catalog/

## 📋 包含字段

### 文本模型 (index.html)

| 字段 | 说明 |
|------|------|
| 模型厂商 | OpenAI / Anthropic / Google / Meta / DeepSeek / 豆包 / 通义千问 / 智谱AI / MiniMax / 商汤 SenseNova / 月之暗面 / 小米 / 腾讯混元 / xAI / 美团 / 讯飞星火 |
| 模型名称 | 含版本号 |
| 模型参数量 | 已公开的标注 |
| 最大输入 | 上下文窗口长度 |
| 最大输出 | 单次输出 token 上限 |
| 输入价格 | 每百万 token |
| 缓存命中价格 | Prompt Cache 折扣价 |
| 输出价格 | 每百万 token |
| 多模态 | 支持的输入类型（文本/图片/音频/视频） |
| 评分 | Artificial Analysis Intelligence Index v4.3（2026-09-14 快照，全表统一口径，取各模型最高推理强度档） |
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

### 开源模型 (open-source.html)

| 字段 | 说明 |
|------|------|
| 组织 / 厂商 | Meta / OpenAI / Google / Mistral / DeepSeek / 阿里通义 / 智谱 / 月之暗面 / MiniMax / 腾讯混元 / 百度文心 / 小米 / 阶跃星辰 / 美团 / 讯飞星火 / 面壁 / 上海 AI Lab / 微软 / NVIDIA / IBM / xAI 等 |
| 模型 | 含版本与规模标识 |
| 类别 | 💬 文本/推理 · 🌟 全模态 · 👁️ 视觉语言 · 🎥 视频生成 · 🖼️ 图像/3D 生成 · 💻 代码/Agent |
| 参数量 | 总参数 / MoE 激活参数 |
| 上下文 | 原生上下文长度（含可扩展） |
| 开源协议 | Apache 2.0 / MIT（宽松）· 可商用附条款 · 非商用或营收门槛 |
| 部署门槛 | 常见推理精度下的显存估算（单卡 16GB ~ 多机集群） |
| 特点 | 模型定位与代表能力 |
| 仓库 | Hugging Face / GitHub 链接 |

## ✨ 功能特性

- 🔍 实时搜索：按模型名或厂商筛选
- 🏷️ 快捷筛选：全部 / 国产 / 海外 / 极致低价 / 旗舰
- ↕️ 列排序：点击表头按价格、评分、上下文等排序
- 💡 价格高亮：绿色=低价、橙色=中等、红色=高价
- 📱 响应式布局：移动端可横向滚动

## 📊 数据来源

- 定价数据：各厂商官方定价页面
- 评分数据：[Artificial Analysis](https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index) Intelligence Index **v4.3**（2026-09-14 快照，全表统一口径，取各模型最高推理强度档 max / high）
- 多模态能力：各厂商官方文档
- 开源模型：各组织官方模型卡与仓库 README（协议与参数以官方为准）

## 🗓️ 更新记录

- **2026-09-14**（本轮核查窗口 9/7–9/14）：
  - DeepSeek：新增 **V4.1 Flash**（9/10 12:00 发布并同步生效新价，API 模型名 `deepseek-flash`；552B MoE + CED 因果编码-解码非对称架构，输入激活 8B / 输出激活 16B，1M 上下文 / 384K 输出，原生文本 + 图像输入，MIT 开源，AA v4.3 智能指数 40）
  - DeepSeek 定价：高峰 ¥2 输入 / ¥0.04 缓存命中 / ¥8 输出，空闲时段半价（¥1 / ¥0.02 / ¥4）；相比 V4 Flash 缓存命中降 7 倍多、输出降三分之二
  - DeepSeek 移除 2 款已下线模型：V4 Flash、V4 Flash Vision-Exp（9/10 下线，旧模型名暂时路由到 V4.1 Flash）
  - DeepSeek：**保留 V4 Pro 0813**（处下线过渡期，自 9/14 12:00 起 `deepseek-v4-pro` 请求统一路由至 V4.1 Flash 并按新价计费；条目标注该状态，V4.1 Pro 上线后恢复独立计费）
  - 月之暗面：Kimi K2.7 Code → **Kimi K2.8 Preview**（9/11 全量上线 Kimi Code，综合性能接近 K3，thinking 效率较 K2.7 Code 显著改善，1M 上下文对全部会员档位开放；Model ID `kimi-for-coding` 不变、计费沿用原档位）
  - 智谱：修正 GLM-5.3-Flash 价格 ¥2 / ¥0.5 缓存 / ¥8 → **¥0.8 / ¥0.23 缓存 / ¥2.8**（与官方文档及 8/26 发布口径一致）
  - 音视频：新增 OpenAI **GPT-Live-1**（9/10 上线 API，全双工语音，单模型边听边说、可被打断、推理与工具调用委派给后端模型、支持电话场景；语音层 $0.05/分钟按秒计费，后端模型与工具调用另计）；Google Lyria 3 → **Lyria 3.5**（9/4 上线 Gemini 与 API，完整曲式 + 可提交自写歌词 + 44.1kHz 立体声，$0.08/首）
  - 开源模型：新增 DeepSeek-V4.1-Flash（MIT，原生视觉理解，全局 KV Cache 压至 890 bytes/token，官方面向约 2000 卡级部署合作）；移除被其取代的 DeepSeek-V4-Flash，保留 DeepSeek-V4-Pro（下线过渡期）
  - **评分口径统一**：全部 48 款文本模型改用 Artificial Analysis Intelligence Index **v4.3**（2026-09-14 快照），取各模型最高推理强度档（max / high）分数，原先 v4.1.1 / v4.2 / v4.3 混用导致的跨版本不可比问题已消除
  - 评分变化（v4.1.1/v4.2 → v4.3）：Claude Fable 5.1 66 → 53、GPT-6 Astra 61.2 → 53、Claude Opus 5 63 → 51、Meta Muse Spark 1.3 61 → 48、GPT-5.6 Sol 61 → 47、GLM-5.3 60 → 45、Grok 4.6 61 → 44、Kimi K3 60 → 44、GPT-5.6 Terra 57 → 42、Gemini 3.8 Flash 59 → 41、Qwen3.8 Max 58 → 40、DeepSeek V4.1 Flash 40、GLM-5.3-Flash 补充 42；GLM-5.2 53 → 34、Gemini 3.7 Flash 56 → 39、Claude Sonnet 5 55 → 38、DeepSeek V4 Pro 53 → 36、MiniMax M3 43.4 → 30、Hy3 42 → 26、MiMo V2.5 Pro 45.5 → 26、LongCat-2.0 34 → 20 等
  - 评分留空：AA v4.3 未收录或无可对应档位的模型（Qwen3.7 Max、GPT-5.5、豆包 Seed 系列、商汤 SenseNova 系列、Spark X2.5、Hy4 preview、MiniMax M2.7、Kimi K2.8 Preview、Claude Mythos 5.1、GPT-5.5 Pro）
  - 已核查 OpenAI / Anthropic / Google / Meta / xAI / 阿里通义 / 智谱 / MiniMax / 豆包 / 腾讯混元 / 商汤 / 小米 / 美团 / 讯飞星火：本窗口内除上述条目外无新文本模型发布。Google Gemini 3.8 Flash Cyber（9/2）仅通过 Fairwind Program 向受信任防御方开放、未公开定价，暂不收录
- **2026-09-07**：
  - OpenAI：新增 GPT-6 Astra（9/3 发布、9/5 上线 API，`gpt-6-astra`，1.05M 输入 / 128K 输出，$10 / $1 缓存 / $50，文本 + 图像输入，AA v4.2 智能指数 61.2，位列第二仅次于 Claude Fable 5.1）
  - OpenAI：同步修正 GPT-5.6 系列价格——Sol $5/$30 → $4/$20（8/21 官降）、Terra $2.5/$15 → $2/$12、Luna $1/$6 → $0.2/$1.2（7/31 官降 80%）
  - 新增厂商「讯飞星火」：Spark X2.5（9/7 发布，293B MoE / 30B 激活，全国产算力训练，256K 上下文，覆盖 200+ 语种，强化代码与 Agent，¥1.6 / ¥0.24 缓存 / ¥6，已上线讯飞星辰 MaaS）
  - 开源模型：新增讯飞（词元星火）Spark-X2.5-4B 与 Spark-X2.5-1.7B（9/1 开源，Apache 2.0，混合注意力架构，端侧首个原生 100 万 Token 上下文）
- **2026-09-03**：
  - 新增 Meta 厂商：Muse Spark 1.3（9/2 发布，1M 上下文，文本 + 图像输入，$1.25 / $0.15 缓存 / $4.25，AA 智能指数 61，与 GPT-5.6 Sol、Grok 4.6 并列第三）
  - Google：新增 Gemini 3.8 Flash（9/2 GA，1M 输入 / 64K 输出，文本 / 图像 / 音频 / 视频，$0.75 / $0.075 缓存 / $3.75 年底前推广价，AA 59）；Gemini 3.7 Flash 补充 AA 56
  - 开源模型：新增 Meta Muse Glimmer（30B Dense 开放权重，Apache 2.0，端侧 Agent 定位）
  - 移除 Google 两款旧模型：Gemini 3.5 Flash、Gemini 3.5 Flash-Lite（Flash 线已迭代至 3.8，Google 段保留 3.8 Flash / 3.7 Flash / 3.6 Flash / 3.1 Pro 共 4 款）
- **2026-09-02**：
  - Anthropic：新增 Claude Fable 5.1（Mythos 级旗舰，1M 输入 / 128K 输出，$10 / $0.25 缓存 / $50，AA 智能指数 66，登顶 AA 榜单）；新增 Claude Mythos 5.1（同权重低防护版，仅面向网络安全与生命科学的可信访问计划开放）；新增 Claude Opus 5（1M / 128K，$5 / $0.5 缓存 / $25，AA 63）
  - 移除 Claude Fable 5 与 Claude Opus 4.8（分别由 Fable 5.1、Opus 5 接替）；Fable 5.1 缓存读取较上代降价 75%（$1 → $0.25）
  - 阿里通义：Qwen3.8 Flash 补充 AA 智能指数 56，标注为 Qwen4 架构预览版（125B MoE / 6B 激活，原生多模态）
  - 开源模型：新增 Qwen3.8-2.4T-A95B（2.4T MoE / 95B 激活，1M 上下文，Qwen 社区许可）、Qwen3.8-Flash-Next（125B MoE / 6B 激活，Qwen4 架构预览，256K，AA 56）、Qwen3.8-27B（27B Dense 原生视觉语言，Apache 2.0）
  - 音视频：万相升级至 Wan3.0-Video（All-in-One 全能参考，支持文本/图像/视频/音频/文件输入，单次 30 秒，¥0.3–1.2 元/秒），图像升级至 Qwen-Image-3.0（¥0.18/张起）；移除 Wan2.7-I2V、Wan2.7-VideoEdit、Qwen-Image-2.0
  - 智谱：GLM-5.3-Flash 补充参数量 320B MoE（18B 激活）
  - 已核查 OpenAI / DeepSeek / 月之暗面 / MiniMax / 字节豆包 / 腾讯混元 / xAI，本周期内无新文本模型发布（Google Gemini 3.8 Flash 与 Meta Muse Spark 1.3 于 9/2 夜间发布，见 9-03 记录）
- **2026-08-31**：
  - 新增开源模型清单页面 [`open-source.html`](./open-source.html)：覆盖 26 家组织、55 款开放权重模型，含参数量 / 激活参数 / 上下文 / 开源协议 / 部署显存估算 / 仓库链接
  - 支持按 国产 / 海外 / MoE / Dense / 可商用 / 单卡可跑 / 旗舰 / 多模态 快捷筛选，表头可按参数量、上下文、显存数值排序
  - 三个页面顶部导航互相打通：文本模型 ↔ 音视频模型 ↔ 开源模型
  - 阿里通义：新增 Qwen3.8 Flash（125B MoE / 6B 激活，992K 输入 / 128K 输出，¥0.8 / ¥0.1 缓存 / ¥2.7，8/27 降价后价格）
  - 移除 Qwen3.6 Flash、GLM-5V-Turbo、GLM-5.1、GLM-5-Turbo、Kimi K2.6、Gemini 3.1 Flash-Lite 共 6 款旧模型
- **2026-08-28**：
  - 腾讯混元：新增 Hy4 preview（770B MoE / 49B 激活，1M 上下文，已开源，¥6 / ¥0.3 缓存 / ¥18）
  - DeepSeek：新增 V4-Flash-Vision-Exp 多模态视觉模型（首次支持图片输入，1M / 384K）；全系改为峰谷计价，表中更新为高峰价（V4-Flash ¥3.2/¥0.1/¥9.6、V4-Pro ¥9.6/¥0.32/¥28.8），空闲时段半价
  - 智谱：新增 GLM-5.3（753B，1M / 128K，¥8 / ¥2 缓存 / ¥28，AA 智能指数 60）与 GLM-5.3-Flash（原生多模态，1M / 128K）
  - Google：新增 Gemini 3.7 Flash（最智能 workhorse 模型，1M / 64K，限时半价 $0.75 / $0.075 缓存 / $3.75）
- **2026-08-13**：
  - DeepSeek V4 Pro 正式版（DeepSeek-V4-Pro-0813）确认上线：1M 上下文、384K 输出、默认开启 thinking 模式，价格维持 ¥3 / ¥0.025(缓存) / ¥6（与现有条目一致，无需调整）
  - 新增 xAI Grok 4.6 文本模型（500K 上下文，$2 / $6 定价），原 Grok 4.5 保留并降为常规档
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
