# Agent 商业世界分享：Slide Like Image 全局风格控制

这份文档用于统一整套分享中所有章节配图的视觉语言。每一章单独写图片 prompt 时，都应默认继承这份风格控制，再叠加本章内容。

补充说明：当前这套 prompt 默认按 **GPT Image 系列模型** 的强项来写。根据 OpenAI 目前公开文档，官方主名是 `gpt-image-1 / GPT Image 1.5`，其特点是 **strong prompt adherence、accurate text rendering、high-fidelity editing、real-world knowledge**；同时官方也提醒，复杂布局中的精确文字排版仍可能偶尔失误。因此，prompt 应主动利用它在 **高拟真 UI、网页截图、产品界面、仪表盘、清晰短文本标签** 方面的优势，而不要把它当成纯抽象概念画模型来使用。

## 风格目标

- 配图不是海报，不是概念艺术，不是封面插画，而是 **适合演讲页使用的 slide like image**
- 画面需要为标题、要点、图表留出呼吸空间，不能信息过满
- 风格统一、克制、理性，适合技术分享和校园场景
- 强调“结构感、系统感、产业感”，避免过于拟人化或科幻叙事化

## 统一视觉要求

- 横版构图，适合 16:9 演讲页面
- 整体简洁，避免密集小元素和花哨纹理
- 使用大形体、清晰层次、明确留白
- 图像应更像“章节主视觉背景”而不是“完整信息图”
- 可以有抽象结构、节点、流线、模块、界面轮廓，但不要真的塞满文字
- 不要在图里生成可读长文案，最多允许极少量不可读的抽象 UI 占位

## GPT Image Prompt 写法原则

- 优先把图写成：
  - high-fidelity product UI screenshot
  - realistic web app dashboard
  - clean desktop app interface
  - structured control panel
  - modern research workspace
- 如果一张图适合用界面表达，就直接写成界面，而不是抽象海报
- 明确说明：
  - 页面类型
  - 左中右布局
  - 顶部导航
  - 侧边栏
  - 表格列名
  - 卡片区块
  - 图表位置
  - 主次层级
- 如果要生成网页 / dashboard，优先使用短标签、短表头、短按钮文字，避免大段正文
- 如果需要文字，尽量指定为：
  - 简短英文 UI 标签
  - 简短数字
  - 简短标题
  - 清晰表头
- 如果是解释性图片，优先做成：
  - product mockup
  - educational UI
  - analyst dashboard
  - system map inside a software canvas

## 适合 GPT Image 的内容形态

- OpenRouter 风格的模型 provider 列表页
- Stripe / Plaid / Lark 风格的产品控制台
- AI 研究助手工作台
- IDE + side panel + task status 的开发工具界面
- pricing dashboard
- system map embedded in software canvas
- split-screen before/after product UI

## Prompt 书写建议

- 不要只写“画一个很有科技感的图”
- 要明确写：
  - “a realistic product UI screenshot”
  - “a clean enterprise dashboard”
  - “a modern browser-based control panel”
  - “an OpenRouter-like provider comparison page”
  - “a high-fidelity desktop app interface”
- 如果页面里需要表格，直接写清：
  - 有几列
  - 列名是什么
  - 哪一列强调价格
  - 哪一列强调 latency / stability / model name
- 如果页面里需要卡片，直接写清：
  - card grid
  - one featured card
  - muted secondary cards
  - one highlighted metrics strip
- 如果页面里需要图表，写清：
  - line chart
  - stacked bars
  - routing flow
  - layered dependency map

## 文本与排版约束

- 尽量让界面文字短、清楚、有限
- 不要要求生成长段中文正文
- 可以接受少量清晰英文 UI 文本
- 可以接受数字、价格、列名、按钮名
- 如果必须出现文字，应让文字服务版式，而不是承担说明任务
- 真正的说明文字仍由 PPT 正文承担

## 统一色彩

- 主色调：冷白、深蓝、灰蓝、少量青色
- 整体偏理性、现代、清洁
- 可有少量发光，但只作为强调，不要霓虹泛滥
- 避免紫色主导、粉色主导、橙红色主导
- 避免纯黑赛博朋克夜景

## 统一风格关键词

- editorial tech visual
- abstract systems diagram aesthetic
- calm high-end enterprise AI
- clean layered composition
- restrained futuristic
- strategic technology presentation

## 明确避免

- 不要机器人站在画面中央
- 不要夸张人脸、眼睛、大脑、机械手
- 不要赛博朋克街景
- 不要过强 3D 游戏感
- 不要廉价科幻海报感
- 不要过多拟物芯片、电路板、城市夜景拼贴
- 不要画得像投资广告或创业招商海报

## 画面结构建议

- 每章画面都应围绕“一个核心结构”组织，而不是围绕“一个角色”组织
- 优先使用：
  - 分层结构
  - 网络结构
  - 模块之间的流动关系
  - 从上到下或从中心向外扩展的系统感
- 允许适当出现：
  - 聊天框轮廓
  - IDE 轮廓
  - 浏览器轮廓
  - 文档 / 表格 / 终端 / 云 / 数据节点等抽象符号
- 这些元素都应服务结构，而不是堆砌图标

## 输出标准

- 一眼看上去像同一套 deck 的章节配图
- 每张图都有清晰的主结构
- 颜色和光感统一
- 适合铺在 PPT 页面上并叠标题文字
- 视觉上高级、克制、专业
