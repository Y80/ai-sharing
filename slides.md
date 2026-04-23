---
theme: default
title: AI / LLM / Agents
info: 面向前端团队的一次内部分享
class: text-center home-slide
colorSchema: light
drawings:
  persist: false
transition: slide-left
enableSlideProgress: true
---

# AI / LLM / Agents

<div class="home-subtitle">面向前端团队的一次内部分享</div>

<div class="abs-br m-6 flex gap-2 text-sm deck-meta deck-meta-pill">
  <img src="/imgs/icons/sparkles.svg" class="inline w-4 h-4" />
  <span>2026.04</span>
</div>

---
class: question-slide
---

# 三个核心问题

<div class="question-grid mt-8">
  <div class="border rounded p-7 question-card">
    <span class="question-index">01</span>
    <p><strong>AI 编程是怎样一步步演化到今天这个阶段的？</strong></p>
  </div>
  <div class="border rounded p-7 question-card">
    <span class="question-index">02</span>
    <p><strong>智能体到底强在什么地方？它和普通对话式 AI 的区别是什么？</strong></p>
  </div>
  <div class="border rounded p-7 question-card">
    <span class="question-index">03</span>
    <p><strong>在实际工程里，我们应该怎样跟 AI 协作，才能既提效，又不失控？</strong></p>
  </div>
</div>

---

# AI 编程的进化路线图

<div class="grid grid-cols-3 gap-8 mt-12">

<div class="border rounded p-6 text-center">

### 阶段一<br>代码补全

<img src="/imgs/icons/keyboard.svg" class="w-10 h-10 mt-4 opacity-30 mx-auto" />

<div class="text-sm mt-4">Tabnine · Copilot</div>
<div class="text-xs mt-2 opacity-60">按 Tab 接受建议</div>

</div>

<div class="border rounded p-6 text-center">

### 阶段二<br>对话副驾驶

<img src="/imgs/icons/messages-square.svg" class="w-10 h-10 mt-4 opacity-30 mx-auto" />

<div class="text-sm mt-4">Cursor · Trae</div>
<div class="text-xs mt-2 opacity-60">项目级工程视野</div>

</div>

<div class="border rounded p-6 text-center feature-card">

### 阶段三<br>智能体工作流

<img src="/imgs/icons/bot.svg" class="w-10 h-10 mt-4 opacity-30 mx-auto" />

<div class="text-sm mt-4">Claude Code · Codex · OpenCode</div>
<div class="text-xs mt-2 opacity-60">自主行动 · 闭环验证</div>

</div>

</div>

---
class: stage-slide
---

<div class="stage-watermark">
  <img src="/imgs/icons/keyboard.svg" />
</div>

# 阶段一：代码补全时代

<div class="stage-head">
  <span>从「补全几行代码」开始</span>
</div>

<div class="grid grid-cols-2 gap-6 mt-8">
  <div class="border rounded p-6">
    <strong>工具代表</strong>
    <p>Tabnine、GitHub Copilot，以 VS Code 插件形态为主。</p>
    <strong>核心特征</strong>
    <p>按 Tab 接受建议，本质上仍是局部上下文上的概率补全。</p>
  </div>
  <div class="border rounded p-6">
    <strong>人类角色</strong>
    <p>开发工程师仍然负责完整理解工程，AI 主要帮忙省输入成本。</p>
    <strong>功能边界</strong>
    <p>像“瞎子摸象”，只理解光标附近几行代码，缺少全局视角。</p>
  </div>
</div>

<div class="mt-8 border rounded p-4 bg-gray-50">

```ts
function debounce(  // ← 你输入到这里
  // AI 自动补全整个函数 ↓
```

</div>

---
class: stage-slide
---

<div class="stage-watermark">
  <img src="/imgs/icons/messages-square.svg" />
</div>

# 阶段二：对话副驾驶时代

<div class="stage-head">
  <span>从单文件补全走向项目级协作</span>
</div>

<div class="grid grid-cols-2 gap-6 mt-8">
  <div class="border rounded p-6">
    <strong>工具代表</strong>
    <p>Cursor、Trae，既可以是插件，也可以是独立 IDE。</p>
    <strong>能做什么</strong>
    <ul>
      <li>粘贴报错信息让 AI 分析问题</li>
      <li>描述需求文档让 AI 实现功能</li>
      <li>引入关键代码行、文件或图片</li>
    </ul>
  </div>
  <div class="border rounded p-6">
    <strong>核心特征</strong>
    <p>AI 开始拥有项目级工程视野，也开始结合 MCP、Skills。</p>
    <strong>真实限制</strong>
    <ul>
      <li>复杂任务仍然不太敢直接放手</li>
      <li>生成代码需要认真 review</li>
      <li>提示词质量会直接影响结果</li>
    </ul>
  </div>
</div>

<div class="mt-6 text-sm opacity-70">

这一阶段的关键词是“能协作了，但还谈不上稳定托付”。

</div>

---
class: stage-slide
---

<div class="stage-watermark">
  <img src="/imgs/icons/bot.svg" />
</div>

# 阶段三：智能体工作流时代

<div class="stage-head">
  <span>从「被动响应」变成「自主行动」</span>
</div>

<div class="grid grid-cols-2 gap-6 mt-8">
  <div class="border rounded p-6">
    <strong>工具代表</strong>
    <p>Claude Code、Codex、OpenCode。</p>
    <strong>爆发背景</strong>
    <ul>
      <li>上下文越来越大</li>
      <li>专业能力明显增强</li>
      <li>价格下降，调用成本可接受</li>
      <li>多模态支持浏览器、终端、图片、网页</li>
    </ul>
  </div>
  <div class="border rounded p-6 feature-card">
    <strong>核心差异</strong>
    <p>它不只是“回答你”，而是会为了完成目标主动调用工具、翻文档、改文件、跑验证。</p>
    <div class="stage-loop">
      <span>计划</span>
      <span>实施</span>
      <span>验证</span>
    </div>
    <p class="opacity-70">真正的分水岭，是它开始走完整闭环，而不是只输出一段建议文本。</p>
  </div>
</div>

---

# 智能体时代的真实场景

<div class="scenario-grid-six mt-7">
  <div class="border rounded p-5 scenario-panel compact">
    <div class="scenario-title">
      <img src="/imgs/icons/bug.svg" class="w-5 h-5" />
      <strong>BUG 修复</strong>
    </div>
    <p>自动在浏览器里复现路径、定位问题、修改代码并验证结果。</p>
  </div>

  <div class="border rounded p-5 scenario-panel compact">
    <div class="scenario-title">
      <img src="/imgs/icons/file-text.svg" class="w-5 h-5" />
      <strong>文档生成</strong>
    </div>
    <p>给一篇 Markdown 或长文档，自动生成统一风格的 PPT。</p>
  </div>

  <div class="border rounded p-5 scenario-panel compact">
    <div class="scenario-title">
      <img src="/imgs/icons/image.svg" class="w-5 h-5" />
      <strong>UI 设计</strong>
    </div>
    <p>截图真实网页效果，在多主题、多端之间来回验证并迭代界面。</p>
  </div>

  <div class="border rounded p-5 scenario-panel compact">
    <div class="scenario-title">
      <img src="/imgs/icons/languages.svg" class="w-5 h-5" />
      <strong>国际化</strong>
    </div>
    <p>沿着现有 i18n 和工程结构，把文案翻译后准确落回对应位置。</p>
  </div>

  <div class="border rounded p-5 scenario-panel compact">
    <div class="scenario-title">
      <img src="/imgs/icons/coins.svg" class="w-5 h-5" />
      <strong>数据分析报告</strong>
    </div>
    <p>批量获取上证所股票数据，生成精美、动态的股票分析报告。</p>
  </div>

  <div class="border rounded p-5 scenario-panel compact">
    <div class="scenario-title">
      <img src="/imgs/icons/git-branch-plus.svg" class="w-5 h-5" />
      <strong>PRD 落地</strong>
    </div>
    <p>给它一份 PRD，先拆任务、再写代码，最后补验证把功能做完。</p>
  </div>
</div>

---

# oh-my-opencode

<img src="/imgs/icons/workflow.svg" class="inline w-6 h-6" /> 一款搭配 OpenCode 使用的多模型智能体编排框架

<div class="grid grid-cols-2 gap-8 mt-8">

<div>

**内置专职智能体**

| 角色 | 职责 |
|------|------|
| **Sisyphus** 西西弗斯 | 主架构师，任务拆解 |
| **Librarian** 图书管理员 | 看文档、找上下文 |
| **Oracle** 神谕 | Code Review，只挑刺 |
| **Frontend Engineer** | 切图、UI 还原 |

</div>

<div>

**不同模型做不同任务**

<ul>
  <li>主架构师 → GPT / Claude 旗舰模型</li>
  <li>图书管理员 → Kimi K2.5（便宜好用）</li>
  <li>前端工程师 → Gemini（擅长视觉）</li>
</ul>

**爆火原因**
<ol>
  <li>被 Anthropic 点名封杀</li>
  <li>不同模型做不同任务，节省花费</li>
  <li>开箱即用，内置 MCP、Skills、提示词和 LPS/AST 工具链</li>
</ol>

</div>

</div>

---

# CC Switch

<img src="/imgs/icons/sliders-horizontal.svg" class="inline w-6 h-6" /> 配置智能体的超实用必备应用

<div class="mt-7 flex justify-center">
  <img src="/imgs/image.png" class="rounded shadow max-h-60" />
</div>

<div class="mt-7 grid grid-cols-3 gap-6">
  <div class="border rounded p-5 text-center switch-card">
    <strong>集中管理</strong>
    <p>供应商、MCP、Skills、提示词</p>
  </div>
  <div class="border rounded p-5 text-center switch-card">
    <strong>API 代理</strong>
    <p>格式转换、故障转移</p>
  </div>
  <div class="border rounded p-5 text-center switch-card">
    <strong>配置同步</strong>
    <p>导入、导出、备份、同步</p>
  </div>
</div>

---

# MCP 与 Skills：Agent 的两套基础设施

<div class="infra-hero mt-8">
  <div class="border rounded p-7 infra-card">
    <div class="infra-icon-row">
      <img src="/imgs/icons/network.svg" class="w-7 h-7" />
      <strong>MCP</strong>
    </div>
    <h3>决定 AI 能做什么</h3>
    <p>它是 AI 的手和脚，决定它能读什么、操作什么、验证什么。</p>
    <div class="text-sm opacity-70">动态的 · 可执行的 · 双向的</div>
  </div>

  <div class="infra-divider">×</div>

  <div class="border rounded p-7 infra-card">
    <div class="infra-icon-row">
      <img src="/imgs/icons/brain.svg" class="w-7 h-7" />
      <strong>Skills</strong>
    </div>
    <h3>决定 AI 该怎么做</h3>
    <p>它是 AI 的脑回路和行为约束，决定它按什么原则推进任务。</p>
    <div class="text-sm opacity-70">静态的 · 约束性的 · 说明性的</div>
  </div>
</div>

<div class="mt-8 border rounded p-5 text-center feature-card">
  比模型接入更重要的，是一套能复用、能约束、能验证的工作流。
</div>

---

# chrome-devtools-mcp

<div class="section-intro">让大模型通过 MCP 直接进入真实浏览器调试现场。</div>

<div class="cdp-grid mt-6">
  <div class="border rounded p-5">
    <strong>Take Snapshot</strong>
    <p>调用 <code>DOMSnapshot.captureSnapshot</code>，把复杂 DOM 压缩成更适合 AI 决策的语义结构。</p>
    <div class="border rounded p-4 bg-gray-50 mt-3 mono-block">
      {<br>
      &nbsp;&nbsp;"tool": "click",<br>
      &nbsp;&nbsp;"arguments": {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"uid": "10_34",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"includeSnapshot": true<br>
      &nbsp;&nbsp;}<br>
      }
    </div>
  </div>

  <div class="border rounded p-5 cdp-side">
    <img src="/imgs/image-1.png" class="snapshot-shot" />
    <div class="mini-meta mt-3">base.md 中的 Take Snapshot 截图</div>
    <div class="capability-list mt-3">
      <div><strong>Take Screenshot</strong><span>基于真实渲染继续判断</span></div>
      <div><strong>Emulate</strong><span>切换设备、主题和网络条件</span></div>
      <div><strong>Evaluate Script</strong><span>执行脚本，拿运行态数据和调试线索</span></div>
    </div>
  </div>
</div>

---

# 常用 MCP

<div class="tool-grid tool-grid-mcp mt-6">
  <div class="border rounded p-5 tool-card">
    <strong>chrome-devtools</strong>
    <p>直接操作浏览器，查看真实渲染结果，并读取 Console、Network 等调试信息。</p>
    <div class="micro-chip-grid mt-3">
      <span>Take snapshot</span>
      <span>Take screenshot</span>
      <span>Emulate</span>
      <span>Evaluate Script</span>
    </div>
  </div>
  <div class="border rounded p-5 tool-card">
    <strong>fetch</strong>
    <p>拉取网页和文档内容，适合查询官方资料、API 说明和错误信息。</p>
  </div>
  <div class="border rounded p-5 tool-card">
    <strong>context7</strong>
    <p>补充最新文档和框架知识，适合处理依赖官方文档上下文的开发任务。</p>
  </div>
  <div class="border rounded p-5 tool-card">
    <strong>数据库操作</strong>
    <p>直接查询或修改数据库，适合排查数据问题、验证状态和处理后台联动场景。</p>
  </div>
</div>

---

# 常用 Skills

<div class="tool-grid tool-grid-skills mt-6">
  <div class="border rounded p-5 tool-card compact">
    <strong>frontend-design</strong>
    <p>补充界面设计方向和视觉约束，适合处理布局、风格和组件表现。</p>
  </div>
  <div class="border rounded p-5 tool-card compact">
    <strong>find-skills</strong>
    <p>帮助 AI 快速找到合适技能集合，减少能力选择上的试错成本。</p>
  </div>
  <div class="border rounded p-5 tool-card compact">
    <strong>upload-images</strong>
    <p>把截图、设计稿或素材变成可继续交给模型处理的输入。</p>
  </div>
  <div class="border rounded p-5 tool-card compact">
    <strong>iconify</strong>
    <p>统一图标选型、接入方式和渲染细节，减少实现过程中的碎判断。</p>
  </div>
  <div class="border rounded p-5 tool-card compact">
    <strong>create-skills</strong>
    <p>辅助创建自定义技能，把行为约束和工作流沉淀下来。</p>
  </div>
  <div class="border rounded p-5 tool-card compact">
    <strong>karpathy-guidelines</strong>
    <p>把 Karpathy 四原则嵌入协作流程，确保智能体按工程规则推进任务。</p>
  </div>
</div>

---

# Skills 为什么和 MCP 缺一不可？

<div class="mt-6 text-lg">以设计一个 UI 精美的登录页为例：</div>

<div class="mt-6 grid grid-cols-2 gap-6">
  <div class="border rounded p-6 bg-green-50">
    <strong>有 Skill + 有 MCP</strong>
    <p>懂得按设计规则去做，也能在浏览器里截图验证、微调和闭环验收。</p>
  </div>
  <div class="border rounded p-6 bg-yellow-50">
    <strong>只有 Skill 没有 MCP</strong>
    <p>单个元素可能看着还行，但缺少真实渲染验证，整体很容易失控。</p>
  </div>
  <div class="border rounded p-6 bg-yellow-50">
    <strong>只有 MCP 没有 Skill</strong>
    <p>它知道怎么打开页面和截图，但不知道什么叫“好设计”。</p>
  </div>
  <div class="border rounded p-6 bg-red-50">
    <strong>既没有 Skill，也没有 MCP</strong>
    <p>结果通常会非常原始，只剩模型默认输出，没有工程感和设计感。</p>
  </div>
</div>

---

# Karpathy 编程四原则

<div class="grid grid-cols-2 gap-6 mt-8">
  <div class="border rounded p-6">
    <strong>编码前思考</strong>
    <p>先说清假设、困惑和取舍，别在错误前提上越跑越远。</p>
  </div>
  <div class="border rounded p-6">
    <strong>简洁优先</strong>
    <p>能用更少代码解决，就不要为了“显得灵活”而过度抽象。</p>
  </div>
  <div class="border rounded p-6">
    <strong>精准修改</strong>
    <p>只碰和目标直接相关的地方，避免顺手改出一堆无关 diff。</p>
  </div>
  <div class="border rounded p-6 feature-card">
    <strong>目标驱动执行</strong>
    <p>先定义什么算成功，再围绕测试、验证和验收标准去推进实现。</p>
  </div>
</div>

<div class="mt-6 text-sm opacity-70">
不是教人怎么“写提示词”，而是教你如何把工程习惯翻译成 Agent 能执行的规则。
</div>

---

# 必须保持清醒的一点

<div class="border rounded p-7 bg-red-50 mt-10">
  <div class="text-2xl font-bold">⚠️ AI 编码代理天然倾向于走最短路径</div>
  <p class="mt-4">最短路径通常意味着跳过规范、测试、安全审查，以及那些真正让软件可靠的工程实践。</p>
</div>

<div class="mt-8 border rounded p-6">
  所以 Agent Skills 的价值，不是把模型变得更聪明，而是让它更像一个成熟工程师，知道哪些步骤不能省、哪些标准必须过。
</div>

---

# 和 AI 协作更稳的三条原则

<div class="grid grid-cols-3 gap-6 mt-10">
  <div class="border rounded p-6">
    <strong>目标说清楚</strong>
    <p>把判断标准、边界条件、不能碰的文件、必须经过的验证步骤讲明白。</p>
  </div>
  <div class="border rounded p-6">
    <strong>流程交出去</strong>
    <p>不要只给抽象目标，要把你平时做事的顺序和检查点也一并交代。</p>
  </div>
  <div class="border rounded p-6">
    <strong>验收抓在手里</strong>
    <p>把“看起来像做完了”改成“有验证地证明做完了”。</p>
  </div>
</div>

---

# 把工作流交代给 AI

<div class="workflow-grid mt-8">
  <div class="border rounded p-6">
    <strong>1. 先理解问题和影响范围</strong>
    <p>告诉它问题背景、相关模块和你最担心的副作用。</p>
  </div>
  <div class="border rounded p-6">
    <strong>2. 再定位代码和上下文</strong>
    <p>让它先找相关文件、关键链路和依赖关系，再进入改动。</p>
  </div>
  <div class="border rounded p-6">
    <strong>3. 再提出修改方案</strong>
    <p>先说明会改什么、为什么这样改，再动手实现。</p>
  </div>
  <div class="border rounded p-6 feature-card">
    <strong>4. 修改后跑验证，再检查副作用</strong>
    <p>把测试、截图、构建、冒烟验证和回归检查明确列出来。</p>
  </div>
</div>

---

# 给 AI 足够新的信息和视觉上下文

<div class="grid grid-cols-2 gap-6 mt-8">
  <div class="border rounded p-6">
    <strong>在线搜索不能缺</strong>
    <p>很多问题依赖最新信息：库版本变化、官方文档更新、兼容性说明、社区 issue。</p>
    <p class="opacity-70">没有在线搜索能力的智能体，更像“记忆里的专家”。</p>
  </div>
  <div class="border rounded p-6">
    <strong>UI / 报错问题尽量带图</strong>
    <p>截图、设计稿、报错图一起给，判断质量会明显提升，因为这些问题本身就高度依赖视觉和上下文。</p>
  </div>
</div>

---

# 从“让它做”到“定义成功”

<div class="mt-8">

| 不要这样说 | 更好的成功标准 |
|------------|----------------|
| 添加验证 | 为无效输入写测试，然后让它们通过 |
| 修复 bug | 先重现 bug，再让它稳定通过 |
| 重构 X | 确保重构前后测试都能通过 |

</div>

<div class="mt-8 border rounded p-5 bg-blue-50">
  “LLM 非常擅长循环执行直到达成特定目标……不要告诉它该做什么，给它成功标准，然后看着它完成。” — Andrej Karpathy
</div>

---

# 如何判断这套协作方式在起作用

<div class="grid grid-cols-2 gap-6 mt-8">
  <div class="border rounded p-6">
    <strong>不必要的 diff 更少</strong>
    <p>只出现和目标直接相关的改动。</p>
  </div>
  <div class="border rounded p-6">
    <strong>过度复杂导致的重写更少</strong>
    <p>代码第一次就更接近“够用且简洁”。</p>
  </div>
  <div class="border rounded p-6">
    <strong>澄清问题更早出现</strong>
    <p>而不是在实现错了以后才发现前提不成立。</p>
  </div>
  <div class="border rounded p-6">
    <strong>PR 更干净</strong>
    <p>没有顺手的“改进”和无关重构。</p>
  </div>
</div>

---

# 对前端工程师意味着什么

<div class="border rounded p-7 feature-card value-hero mt-7">
  <div class="value-hero-head">
    <img src="/imgs/icons/compass.svg" class="w-7 h-7" />
    <strong>工程师的价值，正在从「代码产出速度」转向「决策质量」</strong>
  </div>
  <p>用了智能体之后，那些“想做但嫌麻烦”的念头更容易被快速落地，但真正稀缺的不是打字速度，而是判断力。</p>
</div>

<div class="value-split mt-6">
  <div class="border rounded p-6">
    <strong>越来越不稀缺</strong>
    <ul>
      <li>快速写代码的能力</li>
      <li>机械性的键盘输入</li>
      <li>单纯的代码产出量</li>
    </ul>
  </div>
  <div class="border rounded p-6 feature-card">
    <strong>越来越值钱</strong>
    <ul>
      <li>判断需求是否合理</li>
      <li>设计方案是否成立</li>
      <li>实现路径是否稳妥</li>
      <li>生成结果是否可靠</li>
    </ul>
  </div>
</div>

---

# 一个不太严谨但很好懂的比喻

<div class="analogy-grid mt-10">
  <div class="border rounded p-8 analogy-card">
    <img src="/imgs/icons/book-open-text.svg" class="w-12 h-12 mb-5 mx-auto" />
    <h3>LLM</h3>
    <p>像一个掌握了很多数学定理的学生。</p>
    <p class="opacity-70">知道很多知识点，但刷题不够多，遇到复杂问题时，不一定知道这些定理该怎样组合使用。</p>
  </div>
  <div class="analogy-arrow">→</div>
  <div class="border rounded p-8 analogy-card feature-card">
    <img src="/imgs/icons/bot.svg" class="w-12 h-12 mb-5 mx-auto" />
    <h3>智能体</h3>
    <p>像你在旁边不断给它提示。</p>
    <p class="opacity-70">这一步先看条件，这一步先做验证，这一步再用哪个方法，于是它终于有机会把复杂题真的做出来。</p>
  </div>
</div>

---

# 真正的竞争力

<div class="border rounded p-8 feature-card mt-14 text-center">
  <div class="text-3xl font-bold leading-tight">未来竞争力 = 能不能带着 AI<br>稳定地产出正确结果</div>
  <p class="mt-6 text-lg">不是提示词花样更多，而是更会表达目标、约束流程、建立标准、做出判断。</p>
</div>

---

# 三个收尾结论

<div class="grid grid-cols-3 gap-6 mt-10">
  <div class="border rounded p-6">
    <strong>1. AI 编程已经进入智能体工作流时代</strong>
    <p>真正的变化，不只是模型更强，而是它具备了行动能力和验证能力。</p>
  </div>
  <div class="border rounded p-6">
    <strong>2. 前端团队值得重点关注这波变化</strong>
    <p>浏览器、视觉、交互、多端适配，天然就是智能体最容易形成闭环的场景。</p>
  </div>
  <div class="border rounded p-6 feature-card">
    <strong>3. 工程师最需要升级的是判断力</strong>
    <p>表达目标、约束流程、建立验收标准，会比“写得快”更重要。</p>
  </div>
</div>

---
class: finale-slide
---

# 谢谢大家

<div class="finale-sub">欢迎继续交流 AI / LLM / 智能体协作实践</div>
