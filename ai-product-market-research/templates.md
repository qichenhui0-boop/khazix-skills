# HTML报告模板

## 完整HTML骨架

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>[报告标题] — 横纵分析法深度研究报告</title>
<style>
  /* 完整CSS见下方"样式系统"章节 */
</style>
</head>
<body>

<div class="progress-bar" id="progressBar"></div>

<!-- 封面 -->
<section class="cover">
  <h1>[报告主标题]</h1>
  <p class="subtitle">[副标题：横纵分析法深度研究报告]</p>
  <div class="divider"></div>
  <div class="meta-line">
    研究时间：[年月]（最后更新：[具体日期]）<br>
    所属领域：[领域]<br>
    研究对象类型：[概念 / 产品形态 / 市场格局]
  </div>
  <div class="scroll-hint">向下滚动开始阅读<span>&#8595;</span></div>
</section>

<!-- 目录 -->
<nav class="toc-section">
  <h2>目录</h2>
  <ul class="toc-list">
    <li><a href="#def"><span class="toc-num">01</span><span class="toc-label">一句话定义</span><span class="toc-arrow">&#8594;</span></a></li>
    <li><a href="#vertical"><span class="toc-num">02</span><span class="toc-label">纵向分析：[纵轴标题]</span><span class="toc-arrow">&#8594;</span></a></li>
    <li><a href="#horizontal"><span class="toc-num">03</span><span class="toc-label">横向分析：[横轴标题]</span><span class="toc-arrow">&#8594;</span></a></li>
    <li><a href="#cross"><span class="toc-num">04</span><span class="toc-label">横纵交汇洞察</span><span class="toc-arrow">&#8594;</span></a></li>
    <!-- 可选章节 -->
    <li><a href="#strategic"><span class="toc-num">05</span><span class="toc-label">[特定产品]的演进路径与终局形态</span><span class="toc-arrow">&#8594;</span></a></li>
    <li><a href="#sources"><span class="toc-num">06</span><span class="toc-label">信息来源</span><span class="toc-arrow">&#8594;</span></a></li>
  </ul>
</nav>

<!-- 正文 -->
<main class="content-wrapper">

  <!-- 一句话定义 -->
  <div class="definition-card" id="def">
    [用一句话概括整个研究的核心发现。这句话应该精炼到可以被引用和传播。]
  </div>

  <!-- 纵向分析 -->
  <div class="section-header" id="vertical">
    <div class="section-sub">Part 02 &middot; Diachronic Analysis</div>
    <h2>纵向分析：[从A到B的演进]</h2>
  </div>
  <!-- 章节配图 -->
  <img src="images/[图片名].png" alt="[描述]" class="section-illustration">
  <p class="illustration-caption">[图片说明]</p>
  <!-- 内容用h3分节 -->
  <h3>2.1 [小节标题]</h3>
  <p>[叙事体正文...]</p>

  <!-- 横向分析 -->
  <div class="section-header" id="horizontal">
    <div class="section-sub">Part 03 &middot; Synchronic Analysis</div>
    <h2>横向分析：[当前竞争图谱标题]</h2>
  </div>
  <!-- 产品对比表格 -->
  <div class="table-wrapper">
    <table>
      <thead><tr><th>维度</th><th>产品A</th><th>产品B</th><th>产品C</th></tr></thead>
      <tbody>
        <tr><td>技术路线</td><td>...</td><td>...</td><td>...</td></tr>
      </tbody>
    </table>
  </div>

  <!-- 横纵交汇 -->
  <div class="section-header" id="cross">
    <div class="section-sub">Part 04 &middot; Cross-Axis Synthesis</div>
    <h2>横纵交汇洞察</h2>
  </div>

  <!-- 可选：特定产品演进 -->
  <!-- 如有第五章针对特定产品的分析，在此插入 -->

  <!-- 总结章节模板（必需） -->
  <!--
    总结部分必须包含两个层次：
    1. 行业级趋势总结：底层规律 → 结构性拐点 → 并行路径 → 终局变量 → 多层竞争全景
    2. 特定产品战略定位（如适用）：在趋势画布上标注具体产品的位置和路径
  -->
  <h3>X.Y 总结：行业演进趋势与[产品名]的战略定位</h3>

  <h4>整体演进趋势</h4>
  <p>[底层规律：从纵轴全历史提炼的不变量——"谁控制X谁控制Y"]</p>
  <p>[结构性拐点：当前正在发生的不可逆结构变化——"A和B正在分离/融合"]</p>
  <p>[并行演进路径：2-4条路径及各自时间窗口和终局推演]</p>
  <p>[终局变量：决定胜负的根本因素——通常是商业模式而非技术]</p>
  <p>[多层竞争全景：表面→深层→根本三层竞争同时展开的判断]</p>

  <h4>[产品名]的战略定位</h4>
  <div class="highlight-box">
    <strong>[产品名]在[时代]的最佳演进路径：</strong>[在趋势画布上定位，结合信任/确定性/ROI等TO B关切，给出具体路径和终局形态]
  </div>

  <!-- 信息来源 -->
  <div class="sources" id="sources">
    <h2>信息来源</h2>
    <ol>
      <li>[来源1]</li>
      <li>[来源2] — <a href="[URL]" target="_blank">[域名]</a></li>
    </ol>
  </div>

</main>

<footer class="report-footer">
  本报告使用横纵分析法（Horizontal-Vertical Analysis）框架完成。
</footer>

<button class="back-top" id="backTop" onclick="window.scrollTo({top:0,behavior:'smooth'})">&#8593;</button>

<script>
window.addEventListener('scroll', () => {
  const h = document.documentElement;
  const pct = (h.scrollTop / (h.scrollHeight - h.clientHeight)) * 100;
  document.getElementById('progressBar').style.width = pct + '%';
  document.getElementById('backTop').classList.toggle('visible', h.scrollTop > 600);
});
</script>
</body>
</html>
```

## 样式系统（CSS）

以下是经过验证的完整CSS样式系统，直接内嵌到HTML的`<style>`标签中。

### 设计原则
- 配色：深蓝(#1a5276)为主色、绿色(#1e8449)为副色、紫色(#5b2c6f)为第三色
- 字体：Noto Serif SC用于标题，Noto Sans SC用于正文
- 行高：正文1.85，确保中文阅读舒适度
- 最大宽度：正文区域780px，目录区域720px
- 圆角：统一12px（小元素8px）

### 完整CSS

```css
@import url('https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;600;700&family=Noto+Sans+SC:wght@300;400;500;700&display=swap');

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --deep-blue: #1a5276;
  --green: #1e8449;
  --light-blue: #2e86c1;
  --purple: #5b2c6f;
  --dark: #2c3e50;
  --mid-gray: #5d6d7e;
  --light-gray: #95a5a6;
  --bg: #fafbfc;
  --card-bg: #ffffff;
  --border: #e8ecf1;
  --accent-bg: #f0f4f8;
}

html { scroll-behavior: smooth; font-size: 16px; }

body {
  font-family: 'Noto Sans SC', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  color: var(--dark);
  background: var(--bg);
  line-height: 1.85;
  -webkit-font-smoothing: antialiased;
}

/* 封面 */
.cover {
  min-height: 100vh;
  display: flex; flex-direction: column; justify-content: center; align-items: center;
  text-align: center;
  background: linear-gradient(160deg, #0f2027 0%, #203a43 40%, #2c5364 100%);
  color: white; padding: 60px 24px; position: relative; overflow: hidden;
}
.cover::before {
  content: ''; position: absolute; top: -50%; left: -50%; width: 200%; height: 200%;
  background: radial-gradient(circle at 30% 50%, rgba(46,134,193,0.12) 0%, transparent 60%),
              radial-gradient(circle at 70% 80%, rgba(30,132,73,0.08) 0%, transparent 50%);
  animation: drift 20s ease-in-out infinite;
}
@keyframes drift { 0%, 100% { transform: translate(0, 0); } 50% { transform: translate(-2%, 1%); } }
.cover > * { position: relative; z-index: 1; }
.cover h1 { font-family: 'Noto Serif SC', serif; font-size: clamp(2rem, 5vw, 3.2rem); font-weight: 700; letter-spacing: 3px; margin-bottom: 16px; line-height: 1.3; }
.cover .subtitle { font-size: 1.1rem; color: rgba(255,255,255,0.6); margin-bottom: 24px; font-weight: 300; }
.cover .divider { width: 80px; height: 2px; background: linear-gradient(90deg, transparent, rgba(255,255,255,0.5), transparent); margin: 0 auto 24px; }
.cover .meta-line { font-size: 0.9rem; color: rgba(255,255,255,0.45); line-height: 1.8; }
.cover .scroll-hint { position: absolute; bottom: 32px; left: 50%; transform: translateX(-50%); color: rgba(255,255,255,0.3); font-size: 0.8rem; animation: bounce 2s infinite; }
.cover .scroll-hint span { display: block; margin-top: 6px; font-size: 1.2rem; }
@keyframes bounce { 0%, 100% { transform: translateX(-50%) translateY(0); } 50% { transform: translateX(-50%) translateY(8px); } }

/* 目录 */
.toc-section { max-width: 720px; margin: 0 auto; padding: 80px 24px 60px; }
.toc-section h2 { font-family: 'Noto Serif SC', serif; font-size: 1.6rem; color: var(--deep-blue); margin-bottom: 32px; text-align: center; }
.toc-list { list-style: none; }
.toc-list li { border-bottom: 1px solid var(--border); padding: 12px 0; }
.toc-list li:last-child { border-bottom: none; }
.toc-list a { display: flex; justify-content: space-between; align-items: center; text-decoration: none; color: var(--dark); font-size: 1rem; transition: color 0.2s; }
.toc-list a:hover { color: var(--light-blue); }
.toc-list .toc-num { display: inline-block; width: 28px; height: 28px; line-height: 28px; text-align: center; background: var(--accent-bg); color: var(--deep-blue); border-radius: 6px; font-size: 0.8rem; font-weight: 700; margin-right: 14px; flex-shrink: 0; }
.toc-list .toc-label { flex: 1; }
.toc-list .toc-arrow { color: var(--light-gray); font-size: 0.8rem; }

/* 正文区域 */
.content-wrapper { max-width: 780px; margin: 0 auto; padding: 0 24px 100px; }

/* 一句话定义卡片 */
.definition-card { background: linear-gradient(135deg, #1a5276 0%, #2e86c1 100%); color: white; border-radius: 16px; padding: 40px 36px; margin: 60px 0 50px; text-align: center; font-size: 1.15rem; line-height: 1.9; font-weight: 400; box-shadow: 0 8px 30px rgba(26,82,118,0.2); }

/* 章节标题 */
.section-header { margin-top: 80px; margin-bottom: 40px; padding-top: 40px; border-top: 3px solid var(--border); }
.section-header:first-of-type { border-top: none; padding-top: 0; margin-top: 40px; }
.section-header h2 { font-family: 'Noto Serif SC', serif; font-size: 1.8rem; color: var(--deep-blue); margin-bottom: 6px; line-height: 1.4; }
.section-header .section-sub { font-size: 0.85rem; color: var(--light-gray); text-transform: uppercase; letter-spacing: 2px; font-weight: 500; }

h3 { font-family: 'Noto Serif SC', serif; font-size: 1.3rem; color: var(--green); margin: 48px 0 16px; line-height: 1.4; }
h4 { font-family: 'Noto Sans SC', sans-serif; font-size: 1.1rem; color: var(--purple); margin: 36px 0 12px; font-weight: 700; }
p { margin-bottom: 16px; color: var(--dark); font-size: 1rem; line-height: 1.85; }
p strong { color: #1a252f; font-weight: 700; }

/* 引用块 */
blockquote, .bq { border-left: 3px solid var(--deep-blue); background: var(--accent-bg); padding: 16px 20px; margin: 20px 0; border-radius: 0 8px 8px 0; color: var(--mid-gray); font-size: 0.95rem; line-height: 1.75; }

/* 黄色高亮框 - 用于重要结论 */
.highlight-box { background: #fef9e7; border: 1px solid #f9e79f; border-radius: 10px; padding: 20px 24px; margin: 24px 0; font-size: 0.95rem; line-height: 1.8; }
.highlight-box strong { color: #7d6608; }

/* 白色卡片 - 用于详细说明 */
.callout { background: white; border: 1px solid var(--border); border-radius: 12px; padding: 24px 28px; margin: 28px 0; box-shadow: 0 2px 12px rgba(0,0,0,0.04); }
.callout-title { font-weight: 700; color: var(--deep-blue); margin-bottom: 8px; font-size: 1rem; }

/* 绿色渐变框 - 用于关键洞察 */
.key-insight { background: linear-gradient(135deg, #eaf2f8 0%, #d5f5e3 100%); border-radius: 12px; padding: 24px 28px; margin: 32px 0; border-left: 4px solid var(--green); }
.key-insight p { color: var(--dark); margin-bottom: 8px; }
.key-insight p:last-child { margin-bottom: 0; }

/* 时间线圆点 */
.timeline-dot { display: inline-block; width: 8px; height: 8px; background: var(--light-blue); border-radius: 50%; margin-right: 8px; vertical-align: middle; }

/* 表格 */
.table-wrapper { overflow-x: auto; margin: 28px 0; border-radius: 12px; box-shadow: 0 2px 12px rgba(0,0,0,0.06); }
table { width: 100%; border-collapse: collapse; font-size: 0.85rem; background: white; }
thead th { background: var(--deep-blue); color: white; padding: 12px 14px; text-align: left; font-weight: 600; font-size: 0.82rem; white-space: nowrap; }
thead th:first-child { border-radius: 12px 0 0 0; }
thead th:last-child { border-radius: 0 12px 0 0; }
tbody td { padding: 10px 14px; border-bottom: 1px solid var(--border); vertical-align: top; line-height: 1.6; }
tbody tr:nth-child(even) { background: #f8fafb; }
tbody tr:last-child td { border-bottom: none; }
tbody tr:last-child td:first-child { border-radius: 0 0 0 12px; }
tbody tr:last-child td:last-child { border-radius: 0 0 12px 0; }

/* 情景卡片 */
.scenario-cards { display: grid; grid-template-columns: 1fr; gap: 20px; margin: 28px 0; }
.scenario-card { border-radius: 12px; padding: 24px 28px; border: 1px solid var(--border); background: white; }
.scenario-card.likely { border-left: 4px solid var(--light-blue); }
.scenario-card.danger { border-left: 4px solid #e74c3c; }
.scenario-card.optimistic { border-left: 4px solid var(--green); }
.scenario-card h5 { font-size: 1rem; margin-bottom: 10px; font-weight: 700; }
.scenario-card.likely h5 { color: var(--light-blue); }
.scenario-card.danger h5 { color: #e74c3c; }
.scenario-card.optimistic h5 { color: var(--green); }
.scenario-card p { font-size: 0.93rem; margin-bottom: 0; color: var(--mid-gray); }

/* 配图 */
.section-illustration { width: 100%; border-radius: 12px; margin: 28px 0; box-shadow: 0 4px 20px rgba(0,0,0,0.08); }
.illustration-caption { text-align: center; font-size: 0.82rem; color: var(--light-gray); margin: -16px 0 28px; font-style: italic; }

/* 信息来源 */
.sources { margin-top: 60px; padding-top: 32px; border-top: 2px solid var(--border); }
.sources h2 { font-family: 'Noto Serif SC', serif; font-size: 1.3rem; color: var(--deep-blue); margin-bottom: 20px; }
.sources ol { padding-left: 24px; color: var(--mid-gray); font-size: 0.85rem; line-height: 2; }
.sources a { color: var(--light-blue); text-decoration: none; }
.sources a:hover { text-decoration: underline; }

/* 页脚 */
.report-footer { text-align: center; padding: 40px 24px 60px; color: var(--light-gray); font-size: 0.82rem; line-height: 1.8; font-style: italic; }

/* 返回顶部 */
.back-top { position: fixed; bottom: 32px; right: 32px; width: 44px; height: 44px; background: var(--deep-blue); color: white; border: none; border-radius: 50%; cursor: pointer; font-size: 1.2rem; display: none; align-items: center; justify-content: center; box-shadow: 0 4px 16px rgba(0,0,0,0.15); transition: opacity 0.3s; z-index: 100; }
.back-top.visible { display: flex; }

/* 进度条 */
.progress-bar { position: fixed; top: 0; left: 0; height: 3px; background: linear-gradient(90deg, var(--deep-blue), var(--light-blue)); z-index: 999; transition: width 0.1s; }

/* 响应式 */
@media (max-width: 600px) {
  .cover h1 { font-size: 1.8rem; }
  .content-wrapper { padding: 0 16px 60px; }
  .definition-card { padding: 28px 20px; font-size: 1rem; }
  table { font-size: 0.75rem; }
  thead th, tbody td { padding: 8px 8px; }
}
```

## 内容组件使用指南

### 1. 一句话定义卡片
用于报告开头，一句话概括核心发现。白字蓝色渐变背景，视觉冲击力强。
```html
<div class="definition-card" id="def">
  [一句话核心发现]
</div>
```

### 2. 章节头（Section Header）
每个大章节的标题区域，包含英文小标和中文标题。
```html
<div class="section-header" id="vertical">
  <div class="section-sub">Part 02 &middot; Diachronic Analysis</div>
  <h2>纵向分析：[标题]</h2>
</div>
```

### 3. 关键洞察框（Key Insight）
蓝绿渐变背景+绿色左边框，用于标记全文最重要的3-5个洞察。
```html
<div class="key-insight">
  <p><strong>一个关键判断：</strong>[洞察内容]</p>
</div>
```

### 4. 高亮框（Highlight Box）
黄色背景，用于总结性结论或"一句话概括"。
```html
<div class="highlight-box">
  <strong>[标签]：</strong>[结论内容]
</div>
```

### 5. 白色卡片（Callout）
白底带阴影，用于详细说明、步骤列表或案例分析。
```html
<div class="callout">
  <div class="callout-title">[卡片标题]</div>
  <p>[内容...]</p>
</div>
```

### 6. 时间线标记
用于纵轴分析中的事件序列。
```html
<p><span class="timeline-dot"></span><strong>2023年3月</strong>，[事件描述]</p>
```

### 7. 对比表格
横向分析的核心组件，用于多产品多维度对比。
```html
<div class="table-wrapper">
  <table>
    <thead><tr><th>维度</th><th>产品A</th><th>产品B</th></tr></thead>
    <tbody><tr><td>[维度名]</td><td>[内容]</td><td>[内容]</td></tr></tbody>
  </table>
</div>
```

### 8. 情景卡片
用于预测或场景分析，三种颜色代表三种可能性。
```html
<div class="scenario-cards">
  <div class="scenario-card likely"><h5>最可能情景</h5><p>[描述]</p></div>
  <div class="scenario-card danger"><h5>风险情景</h5><p>[描述]</p></div>
  <div class="scenario-card optimistic"><h5>乐观情景</h5><p>[描述]</p></div>
</div>
```

### 9. 章节配图
每个主要章节建议配一张概念插图。
```html
<img src="images/[图片名].png" alt="[描述]" class="section-illustration">
<p class="illustration-caption">[图片说明文字]</p>
```

**配图生成Prompt风格**：使用ImageGen生成，风格为"低饱和度、蓝紫色调、科技感概念插画"，尺寸推荐1792x1024（16:9）。

## 配图生成Prompt模板

```
[主题描述], concept illustration, low saturation blue-purple color palette,
clean modern design, abstract geometric elements, soft gradients,
technology and data visualization theme, minimalist style,
no text, no labels, professional quality
```

## 图片目录结构

所有报告配图存放在`outputs/images/`目录下，命名规范：
- `bi_evolution_timeline.png` — 演进时间线
- `competitive_landscape.png` — 竞争图谱
- `cross_axis_insights.png` — 交汇洞察
- `[product]_architecture.png` — 产品架构
- `[concept]_model.png` — 概念模型图
