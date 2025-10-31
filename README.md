项目简介

应用优先的 Clash 规则仓库，同时支持两种使用方式：
- A. 订阅转换（subconverter + .list）
- B. Clash 原生 rule-providers（providers/*.yaml）

上游来源：
- 媒体与去广告：ACL4SSR/ACL4SSR（Clash 规则碎片）
- 基础 RULE-SET 与 CIDR：Loyalsoldier/clash-rules

快速使用

A) 通过 subconverter 生成配置（推荐给已有转换服务）
将 `config=` 指向本仓库 `clash.ini`：
```text
https://HOST/sub?url=你的订阅URL&config=https%3A%2F%2Fcdn.jsdelivr.net%2Fgh%2Fzdev0x%2Fclash-rules%40release%2Fclash.ini
```

B) 直接导入 Clash 配置（rule-providers）
下载并导入：`clash-full.yaml`
- 包含 rule-providers、rules、proxy-groups 占位（需自行填入节点）
- 或把 `clash-rule-providers.yaml` 的 rule-providers 与 rules 合并到你的主配置

规则组（应用优先）
- 🐙 GitHub / ✨ Cursor / 🐳 Docker
- 🤖 OpenAI / 🧠 Gemini / 💬 Claude / 🤖 Copilot
- 🔎 Google（Loyalsoldier）/ 🍎 Apple（Loyalsoldier）
- 📺 国外媒体（ACL4SSR：Netflix/YouTube/DisneyPlus/Spotify）
- ✈️ Telegram（Loyalsoldier Telegram CIDR）
- 💰 Binance

策略与拦截
- 🌐 全球直连：Loyalsoldier direct + `GEOIP,CN`
- 广告拦截（精简）：
  - 自定义：`rulesets/custom/reject.list` 或 `providers/custom/reject.yaml`
  - ACL4SSR：BanAD/BanEasyListChina/BanProgramAD
  - Loyalsoldier：reject.txt
- 🎯 漏网之鱼：`MATCH` 兜底（默认走“🚀 节点选择”）

目录
- `clash.ini`（subconverter）
- `clash-full.yaml`（可直接导入的完整配置）
- `clash-rule-providers.yaml`（可合并进主配置的引用样例）
- `rulesets/*.list`（subconverter 使用）
- `providers/*.yaml`（rule-providers 使用）

致谢
- ACL4SSR/ACL4SSR: https://github.com/ACL4SSR/ACL4SSR
- Loyalsoldier/clash-rules: https://github.com/Loyalsoldier/clash-rules
- SkywalkerJi/Clash-Rules: https://github.com/SkywalkerJi/Clash-Rules

License
- 规则来源遵循各上游项目许可；本仓库文本与示例默认 MIT（可按需更改）
