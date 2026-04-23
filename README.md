# Agent 正在长出怎样的商业世界

这是一套面向校园技术分享的讲稿与配图提示词材料，主题是：

**《Agent 正在长出怎样的商业世界》**

内容目标不是追逐单个热点名词，而是从大模型基础能力出发，解释 Agent 如何从模型、推理、工具、记忆、应用和入口等层次逐步长成一个新的商业世界。

## 文件结构

- `agent_business_world_outline.md`：原料大纲与主题池，保留大量备讲资料、判断和参考信息。
- `agent_business_world_slide_image_style.md`：全局图片生成风格控制，用于统一每章 slide-like image 的视觉风格。
- `agent_business_world_chapter_0_opening.md`：开场问题与总体主线。
- `agent_business_world_chapter_1_llm_foundations.md`：大语言模型的抽象基础能力。
- `agent_business_world_chapter_2_chatbot_to_agent.md`：从 Chatbot 到 Agent。
- `agent_business_world_chapter_3_business_layers.md`：Agent 商业世界的整体层次。
- `agent_business_world_chapter_4_compute_infrastructure.md`：算力 / 基础设施层。
- `agent_business_world_chapter_5_models_inference.md`：模型 / 推理层。
- `agent_business_world_chapter_6_gateway_model_access.md`：Gateway / 模型接入层。
- `agent_business_world_chapter_7_tools_world_connection.md`：工具 / 世界连接层。
- `agent_business_world_chapter_8_context_memory.md`：上下文 / 记忆层。
- `agent_business_world_chapter_9_applications_runtime.md`：应用 / 场景层（含 Agent Runtime）。
- `agent_business_world_chapter_10_entry_distribution.md`：入口 / 分发层。
- `agent_business_world_chapter_11_industry_observations_and_closing.md`：行业观察、去魅与收束。

## 讲述顺序

当前章节按自底向上展开：

1. 先建立大模型和 Agent 的基础认知。
2. 再从算力、模型、Gateway、工具、记忆往上推。
3. 最后进入应用、入口与行业去魅。

这种顺序的目的，是让听众先理解底层能力和成本边界，再理解为什么上层会长出不同的商业角色。

## 图片生成

每个章节末尾都有 `图片生成 Prompts` 区域。生成图片时建议先继承：

`agent_business_world_slide_image_style.md`

再叠加对应章节下的具体图像 prompt。

整体图片风格偏向：

- high-fidelity product UI screenshot
- realistic dashboard
- technical teaching interface
- business analysis slide

用于生成适合作为演示文稿页面的横版 slide-like images。

