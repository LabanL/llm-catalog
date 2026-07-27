# 🤖 2026 大模型 API 清单

实时对比 11 家厂商、40+ 主流大模型的 API 定价、上下文窗口、多模态能力与综合评分。

🔗 **在线访问**：https://labanl.github.io/llm-catalog/

## 📋 包含字段

| 字段 | 说明 |
|------|------|
| 模型厂商 | OpenAI / Anthropic / Google / DeepSeek / 豆包 / 通义千问 / 智谱AI / MiniMax / 月之暗面 / 小米 / 腾讯混元 |
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
