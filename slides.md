---
theme: default
title: AI / LLM / 智能体
info: 面向前端团队的一次内部分享
class: text-center
drawings:
  persist: false
transition: slide-left
enableSlideProgress: true
---

# AI / LLM / 智能体

面向前端团队的一次内部分享

<div class="abs-br m-6 flex gap-2 text-sm">
  <img src="/imgs/icons/sparkles.svg" class="inline w-4 h-4" />
  <span>2026.04</span>
</div>

---

# 三个核心问题

<v-clicks>

1. **AI 编程是怎样一步步演化到今天这个阶段的？**
2. **智能体到底"强"在什么地方？它和普通对话式 AI 的区别是什么？**
3. **在实际工程里，我们应该怎样跟 AI 协作，才能既提效，又不失控？**

</v-clicks>

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

<div class="border rounded p-6 text-center border-blue-500! bg-blue-500/10!">

### 阶段三<br>智能体工作流

<img src="/imgs/icons/bot.svg" class="w-10 h-10 mt-4 opacity-30 mx-auto" />

<div class="text-sm mt-4">Claude Code · Codex</div>
<div class="text-xs mt-2 opacity-60">自主行动 · 闭环验证</div>

</div>

</div>

---

# 阶段一：代码补全时代

<div class="mt-8">

<img src="/imgs/icons/keyboard.svg" class="inline w-6 h-6" /> **工具代表**：Tabnine、Github Copilot（VS Code 插件形态）

**核心特征**：按 Tab 键接受代码建议 — 单向的、基于概率的字符串拼接机器

**人类角色**：开发工程师（AI 只是帮我们省了敲键盘的力气）

</div>

<div class="mt-8 border rounded p-4 bg-gray-50">

```ts
function debounce(  // ← 你输入到这里
  // AI 自动补全整个函数 ↓
```

</div>

<div class="mt-6 text-sm opacity-70">

局限：典型的「瞎子摸象」 — AI 缺少对全局的理解，只理解光标前后几行代码

</div>

---

# 阶段二：对话副驾驶时代

<div class="mt-8">

<img src="/imgs/icons/messages-square.svg" class="inline w-6 h-6" /> **工具代表**：Cursor、Trae（VS Code 插件或独立 IDE）

**核心特征**：打破单文件限制，AI 开始拥有项目级工程视野；结合 MCP、Skills

**人类角色**：开发工程师 ➕ 代码审查员

</div>

<div class="mt-8 grid grid-cols-2 gap-6">

<div class="border rounded p-4">

**能做的事**
- 粘贴报错信息让其分析问题
- 描述需求文档让 AI 实现功能
- 引入关键代码行或文件
- 插入图片辅助理解

</div>

<div class="border rounded p-4">

**局限**
- 不敢布置很有难度的任务
- 生成代码需要认真审查
- 大概率还需要手动调整
- 提示词质量直接影响效果

</div>

</div>

---

# 阶段三：智能体工作流时代

<div class="mt-6 text-xl font-bold"><img src="/imgs/icons/bot.svg" class="inline w-6 h-6" /> 从「被动响应」变成了「自主行动」</div>

<div class="mt-8">

**爆发背景**
- 上下文越来越大，不再只能盯着几百行代码
- 专业能力明显增强
- 价格下降，调用成本可接受
- 多模态支持：文本、图片、网页、终端、浏览器

</div>

<div class="mt-8">

**核心特征**：主动制定计划、调用工具、翻阅文档、操作浏览器、修改文件、运行验证<br>
走完「计划 → 实施 → 验证」的完整闭环

</div>

---

# 智能体时代的真实场景

<div class="grid grid-cols-2 gap-6 mt-8">

<div class="border rounded p-6">

<div class="text-lg font-bold mb-2"><img src="/imgs/icons/bug.svg" class="inline w-5 h-5" /> BUG 修复</div>

描述复现路径，智能体自动在浏览器中操作、定位问题、修改代码、验证结果

</div>

<div class="border rounded p-6">

<div class="text-lg font-bold mb-2"><img src="/imgs/icons/file-text.svg" class="inline w-5 h-5" /> 文档生成</div>

给一篇 Markdown，让智能体自动生成 PPT，统一样式和排版

</div>

<div class="border rounded p-6">

<div class="text-lg font-bold mb-2"><img src="/imgs/icons/image.svg" class="inline w-5 h-5" /> UI 设计</div>

截图网页在亮色/暗色、PC/移动端的实际渲染效果，设计更好的 UI

</div>

<div class="border rounded p-6">

<div class="text-lg font-bold mb-2"><img src="/imgs/icons/languages.svg" class="inline w-5 h-5" /> 国际化</div>

基于项目架构和已有 i18n 体系，把中文文档翻译成其他语言

</div>

</div>

<div class="mt-6 text-sm opacity-70">

这些场景之所以重要：智能体不再只是"给建议"或"补几行代码"，而是真的开始执行任务、调用工具，并对结果负责。

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

- 主架构师 → GPT / Claude 旗舰模型
- 图书管理员 → Kimi K2.5（便宜好用）
- 前端工程师 → Gemini（擅长视觉）

**爆火原因**
1. 被 Anthropic 点名封杀
2. 不同模型做不同任务，节省花费
3. 开箱即用，内置 MCP、Skills、提示词

</div>

</div>

---

# CC Switch

<img src="/imgs/icons/sliders-horizontal.svg" class="inline w-6 h-6" /> 配置智能体的超实用必备应用

<div class="mt-8 flex justify-center">
  <img src="/imgs/image.png" class="rounded shadow max-h-60" />
</div>

<div class="mt-8 grid grid-cols-3 gap-6 text-center">

<div class="border rounded p-4">

**集中管理**
供应商、MCP、Skills、提示词

</div>

<div class="border rounded p-4">

**API 代理**
格式转换、故障转移

</div>

<div class="border rounded p-4">

**配置同步**
导入、导出、备份、同步

</div>

</div>

---

# MCP 与 Skills：Agent 的两套基础设施

<div class="mt-12 flex justify-center gap-16">

<div class="text-center">

<img src="/imgs/icons/network.svg" class="w-12 h-12 mx-auto mb-4" />

### MCP — AI 的「手和脚」

决定 AI 能接触到什么、能操作什么

<div class="text-sm mt-2 opacity-60">动态的 · 可执行的 · 双向的</div>

</div>

<div class="text-center">

<img src="/imgs/icons/brain.svg" class="w-12 h-12 mx-auto mb-4" />

### Skills — AI 的「脑回路」

决定 AI 如何思考，以什么风格做事

<div class="text-sm mt-2 opacity-60">静态的 · 约束性的 · 说明性的</div>

</div>

</div>

<div class="mt-12 text-center text-lg font-bold">

两者缺一不可

</div>

---

# chrome-devtools-mcp

<img src="/imgs/icons/monitor-smartphone.svg" class="inline w-6 h-6" /> 让大模型通过 MCP 与 Chrome DevTools Protocol 通信

<div class="mt-6 text-sm opacity-70">

给了智能体像人一样观察网页、理解网页、操作网页的能力

</div>

<div class="mt-8 grid grid-cols-2 gap-6">

<div class="border rounded p-6">

**Take Snapshot**

调用 `DOMSnapshot.captureSnapshot`<br>
将 DOM 树压缩成精简的语义树

```json
{
  "tool": "click",
  "arguments": {
    "uid": "10_34",
    "includeSnapshot": true
  }
}
```

</div>

<div class="border rounded p-6">

**Take Screenshot**

获取视窗截图、元素截图、整页截图<br>
基于真实渲染结果继续迭代

**Emulate**

模拟移动端/PC端、亮色/暗色模式、网络限制

**Evaluate Script**

执行任意 JavaScript，获取组件实例、DOM 对象引用

</div>

</div>

---

# 对前端实用的 MCP 例子

<div class="grid grid-cols-2 gap-6 mt-8">

<div class="border rounded p-6">

<img src="/imgs/icons/database.svg" class="inline w-5 h-5" /> **filesystem**
读取项目源码、配置文件、路由、样式、i18n 文案，适合跨文件理解和批量修改

</div>

<div class="border rounded p-6">

<img src="/imgs/icons/globe.svg" class="inline w-5 h-5" /> **fetch**
抓官方文档、API 文档、报错说明和兼容性资料。前端生态变化快，实用性很高

</div>

<div class="border rounded p-6">

<img src="/imgs/icons/git-fork.svg" class="inline w-5 h-5" /> **git**
查看提交记录、diff 和历史上下文，适合理解"这段代码为什么这样写"，也适合 Code Review

</div>

<div class="border rounded p-6">

<img src="/imgs/icons/pencil-ruler.svg" class="inline w-5 h-5" /> **Figma MCP**
把设计稿里的节点信息、尺寸、颜色、文案和组件结构带进对话，帮助从设计到代码的落地

</div>

</div>

---

# Skills：为什么和 MCP 缺一不可？

<div class="mt-8">

以设计一个 UI 精美的登录页为例：

</div>

<div class="mt-6 grid grid-cols-2 gap-6">

<div class="border rounded p-6 bg-green-50 border-green-400!">

<img src="/imgs/icons/check-check.svg" class="inline w-5 h-5" /> **有 Skill + 有 MCP**

懂得按设计规则去做，并在浏览器里截图验证、微调、验证，最终得到满意结果

</div>

<div class="border rounded p-6 bg-yellow-50 border-yellow-400!">

⚠️ **只有 Skill 没有 MCP**

单个元素看着还行，但整体依然丑陋

</div>

<div class="border rounded p-6 bg-yellow-50 border-yellow-400!">

⚠️ **只有 MCP 没有 Skill**

能打开页面截图验证，却不知道如何设计好看的页面

</div>

<div class="border rounded p-6 bg-red-50 border-red-400!">

❌ **没有 Skill 也没有 MCP**

设计出来的页面非常原始，毫无设计可言

</div>

</div>

---

# 对前端实用的 Skills 例子

<div class="grid grid-cols-2 gap-6 mt-8">

<div class="border rounded p-6">

<img src="/imgs/icons/sparkles.svg" class="inline w-5 h-5" /> **frontend-design**

给 AI 一套更明确的设计规则，避免产出"默认味很重"的页面

</div>

<div class="border rounded p-6">

<img src="/imgs/icons/blocks.svg" class="inline w-5 h-5" /> **iconify**

统一图标接入方式，快速选择图标，处理不同框架里的渲染方案

</div>

<div class="border rounded p-6">

<img src="/imgs/icons/badge-check.svg" class="inline w-5 h-5" /> **web-design-guidelines**

检查页面的信息层级、视觉一致性、可访问性和交互细节，适合 UI Review

</div>

<div class="border rounded p-6">

<img src="/imgs/icons/lightbulb.svg" class="inline w-5 h-5" /> **karpathy-guidelines**

约束 AI 编码时先思考、少乱改、重验证，尤其适合改生产代码

</div>

</div>

---

# AI 编程时的基本准则

<div class="mt-8 grid grid-cols-2 gap-8">

<div>

### <img src="/imgs/icons/lightbulb.svg" class="inline w-5 h-5" /> 1. 说出来，让 AI 真的懂你

不要把关键信息省略掉。脑子里有判断标准、业务边界、不希望它碰的文件、必须经过的验证步骤 — 都要明确说出来。

越是复杂任务，越不能靠 AI 猜。

</div>

<div>

### <img src="/imgs/icons/workflow.svg" class="inline w-5 h-5" /> 2. 拆解工作流程，交代给 AI

不要只给抽象目标。把你平时自己干活的思考过程拆开来：

1. 先理解问题和影响范围
2. 再定位相关代码和上下文
3. 再提出修改方案
4. 修改完成后跑验证
5. 最后检查是否引入副作用

</div>

<div>

### <img src="/imgs/icons/search.svg" class="inline w-5 h-5" /> 3. 智能体一定要支持在线搜索

很多问题依赖最新信息：库的版本变化、官方文档更新、兼容性说明、社区 issue。没有在线搜索能力的智能体，只是"记忆里的专家"。

</div>

<div>

### <img src="/imgs/icons/image.svg" class="inline w-5 h-5" /> 4. 遇到 UI/交互/报错类问题，尽量给图片

前端很多问题本身就是视觉和上下文敏感的。截图、设计稿、报错截图一起给 AI，判断质量会明显上升。

</div>

</div>

---

# Karpathy 编程四原则

<div class="mt-8">

| 原则 | 解决什么问题 |
|------|-------------|
| <img src="/imgs/icons/brain.svg" class="inline w-4 h-4" /> **编码前思考** | 错误假设、隐藏困惑、缺少权衡 |
| <img src="/imgs/icons/minimize-2.svg" class="inline w-4 h-4" /> **简洁优先** | 过度复杂、臃肿抽象 |
| <img src="/imgs/icons/pencil-ruler.svg" class="inline w-4 h-4" /> **精准修改** | 无关编辑、触碰不应碰的代码 |
| <img src="/imgs/icons/route.svg" class="inline w-4 h-4" /> **目标驱动执行** | 通过测试优先、可验证的成功标准 |

</div>

<div class="mt-8 text-sm opacity-70">

不是教人"怎么写提示词"，而是教你如何把工程上的好习惯，翻译成 Agent 能执行的规则。

</div>

---

# 原则一：编码前先思考

<div class="mt-8 text-xl font-bold"><img src="/imgs/icons/brain.svg" class="inline w-6 h-6" /> 不要假设、妄下断言。不要隐藏困惑。坦诚地权衡利弊。</div>

<div class="mt-8">

- 明确陈述假设
- 若存在多种解释请提出，不要默默做选择
- 若有更简单的方法请提出
- 必要时坚持己见
- 如有疑问请提出

</div>

<div class="mt-8 border rounded p-4 bg-red-50">

⚠️ 模型一旦基于错误假设启动，它会非常努力地在错误方向上一路做下去，而且做得看起来还挺像那么回事。

</div>

---

# 原则二：简洁优先

<div class="mt-8 text-xl font-bold"><img src="/imgs/icons/minimize-2.svg" class="inline w-6 h-6" /> 用最少的代码解决问题。不要进行任何推测。</div>

<div class="mt-8 grid grid-cols-2 gap-6">

<div>

- 没有超出要求的功能
- 不为一次性代码进行抽象
- 没有提供未要求的"灵活性"或"可配置性"
- 对于不可能出现的情况，不进行错误处理

</div>

<div class="border rounded p-4 bg-yellow-50">

**检验标准**

资深工程师会认为这过于复杂吗？如果是，简化它。

如果你写了 200 行，而 50 行就可以写完，那就重写。

</div>

</div>

---

# 原则三：精准修改

<div class="mt-8 text-xl font-bold"><img src="/imgs/icons/pencil-ruler.svg" class="inline w-6 h-6" /> 只碰你必须碰的东西。只清理自己造成的混乱。</div>

<div class="mt-8 grid grid-cols-2 gap-6">

<div>

**改动现有文件时：**
- 不要"改进"相邻的代码、注释或格式
- 不要重构没有问题的代码
- 即使做法不同，也要保持与现有风格一致
- 发现无关死代码 → 指出来，不要删除

</div>

<div>

**当你创建了孤立文件时：**
- 删除因你的修改而不再使用的导入项/变量/函数
- 除非被要求，否则不要删除已有的无效代码

</div>

</div>

<div class="mt-6 text-sm opacity-70">

测试要求：每一行修改后的代码都应该直接追溯到用户的请求。

</div>

---

# 原则四：目标驱动执行

<div class="mt-8 text-xl font-bold"><img src="/imgs/icons/route.svg" class="inline w-6 h-6" /> 定义成功标准。循环验证直至通过。</div>

<div class="mt-8">

| 不要这样做... | 转化为... |
|--------------|----------|
| "添加验证" | "为无效输入编写测试，然后让它们通过" |
| "修复 bug" | "编写重现 bug 的测试，然后让它通过" |
| "重构 X" | "确保重构前后测试都能通过" |

</div>

<div class="mt-8 border rounded p-4 bg-blue-50">

> "LLM 非常擅长循环执行直到达成特定目标……不要告诉它该做什么，给它成功标准，然后看着它完成。" — Andrej Karpathy

</div>

---

# 目标驱动执行：如何判断它在起作用

<div class="mt-8 grid grid-cols-2 gap-6">

<div class="border rounded p-6">

<img src="/imgs/icons/check-check.svg" class="inline w-5 h-5" /> **diff 中不必要的改动更少** — 只有请求的改动出现

</div>

<div class="border rounded p-6">

<img src="/imgs/icons/check-check.svg" class="inline w-5 h-5" /> **因过度复杂而导致的重写更少** — 代码第一次就写得简洁

</div>

<div class="border rounded p-6">

<img src="/imgs/icons/check-check.svg" class="inline w-5 h-5" /> **澄清问题在实现之前提出** — 而不是在犯错之后

</div>

<div class="border rounded p-6">

<img src="/imgs/icons/check-check.svg" class="inline w-5 h-5" /> **干净、精简的 PR** — 没有顺带的重构或"改进"

</div>

</div>

---

# 对前端工程师意味着什么

<div class="mt-8">

用了智能体之后，再次有了刚接触编程时的兴奋感。很多"想做但嫌麻烦"的念头，现在真的有机会快速落地。

</div>

<div class="mt-8 text-xl font-bold">

<img src="/imgs/icons/compass.svg" class="inline w-6 h-6" /> 工程师的价值，正在从「代码产出速度」转向「决策质量」

</div>

<div class="mt-8 grid grid-cols-2 gap-6">

<div>

**越来越不稀缺**
- 快速写代码的能力
- 机械性的键盘输入
- 单纯的代码产出量

</div>

<div>

**越来越值钱**
- 判断需求是否合理
- 设计方案是否成立
- 实现路径是否稳妥
- 生成结果是否可靠

</div>

</div>

---

# 一个不太严谨但很好懂的比喻

<div class="mt-12 flex justify-center gap-16">

<div class="text-center max-w-60">

<img src="/imgs/icons/book-open-text.svg" class="w-12 h-12 mx-auto mb-4" />

### LLM

像一个掌握了很多数学定理的学生

知道很多知识点，但刷题不够多，遇到复杂问题时，不一定知道这些定理该怎样组合使用

</div>

<div class="text-center max-w-60">

<img src="/imgs/icons/bot.svg" class="w-12 h-12 mx-auto mb-4" />

### 智能体

像你在旁边不断给它提示

这一步先看条件，这一步先做验证，这一步再用哪个方法。于是它最终有机会把原本不会做的复杂题，真的做出来

</div>

</div>

---

# 必须保持清醒的一点

<div class="mt-8 border rounded p-6 bg-red-50 text-lg">

⚠️ AI 编码代理天然倾向于走最短路径

最短路径往往意味着跳过规范、跳过测试、跳过安全审查、跳过很多让软件可靠的工程实践

</div>

<div class="mt-8 text-lg">

所以 Agent Skills 这样的机制会越来越重要 — 它不是在帮模型变聪明，而是在帮模型变得更像一个真正成熟的工程师，知道哪些步骤不能省，哪些标准必须过。

</div>

---

# 三个收尾结论

<v-clicks>

1. **AI 编程已经从代码补全 → 对话副驾驶 → 智能体工作流时代**<br>
   真正的变化不只是模型更强了，而是它开始具备「行动能力」和「验证能力」

2. **智能体值得前端团队重点关注**<br>
   它和浏览器、视觉、交互、多端适配这些前端核心场景天然契合<br>
   MCP + Skills 结合后，有机会参与完整的工程闭环

3. **工程师最需要升级的，不是提示词技巧**<br>
   而是如何表达目标、约束流程、建立标准、做出判断<br>
   未来竞争力 = 能不能带着 AI，一起稳定地产出正确结果

</v-clicks>

---

<div class="mt-24 text-center text-2xl font-bold">

谢谢大家 🙏

</div>