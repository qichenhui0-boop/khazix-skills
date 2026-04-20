# Khazix Skills

Agent skills for QoderWork — curated best practices for specialized tasks.

## Skills

### ai-product-market-research

使用横纵分析法对AI时代的产品及竞品进行深度市场研究，生成包含纵向演进分析（产品形态历史与趋势）和横向竞争分析（多维度产品对比）的专业研究报告。

支持 HTML 网页报告 + GitHub Pages 公开网页 + 钉钉文档多格式输出。

**触发场景**: 竞品分析、市场研究、产品研究、行业报告、竞争分析、产品对比、演进分析、赛道分析、产品形态研究。

---

### lingyang-article-writer

为瓴羊 Quick BI 和 Dataphin 撰写专业公众号宣传文章。支持产品宣传文、客户案例、技术解析、趋势洞察、产品对比等多种文章类型。

严格对齐瓴羊品牌风格和 Quick BI 官网设计体系。

**触发场景**: 写公众号文章、Quick BI 文章、Dataphin 文章、产品宣传、功能发布文、客户案例、技术架构文、方法论文章、选型指南。

---

### lingyang-ai-script-writer

撰写瓴羊产品 AI 口播短视频脚本。用于生成符合"痛点前置+观点先行+金句开头"结构的口播文案，适用于数据产品、AI 工具类产品的短视频营销。

**触发场景**: 口播脚本、短视频文案、产品推广脚本。

---

### quickbi-smartq-chat

Quick BI 智能分析技能，支持数据集问数、文件问数、文档解析、仪表板技能生成、数据解读、数据报告等场景。

**触发场景**: 数据分析、问数、智能问数、查数据、分析文件、文档解析、仪表板技能、数据解读、数据报告。

---

## 安装方式

### 一键安装（推荐）

如果你使用 QoderWork，可通过命令行一键安装任意技能：

```bash
# 安装市场研究技能
npx skills add qichenhui0-boop/khazix-skills@ai-product-market-research -g -y

# 安装公众号写作技能
npx skills add qichenhui0-boop/khazix-skills@lingyang-article-writer -g -y

# 安装口播脚本技能
npx skills add qichenhui0-boop/khazix-skills@lingyang-ai-script-writer -g -y

# 安装 Quick BI 智能分析技能
npx skills add qichenhui0-boop/khazix-skills@quickbi-smartq-chat -g -y
```

### 手动安装

1. 克隆此仓库：
```bash
git clone https://github.com/qichenhui0-boop/khazix-skills.git
```

2. 将目标技能文件夹复制到你的 skills 目录：
   - macOS/Linux: `~/.qoderwork/skills/`
   - Windows: `%USERPROFILE%\.qoderwork\skills\`

## 使用方法

安装后，在 QoderWork 中直接描述你的需求即可触发对应技能。

## 报告示例

[AI时代下BI产品的新形态——横纵分析报告](https://qichenhui0-boop.github.io/ai-bi-research-report/)

## License

MIT
