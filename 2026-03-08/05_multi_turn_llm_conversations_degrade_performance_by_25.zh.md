---
title: "Why Multi-Turn Conversations Break Every Top AI Model"
keywords: ["multi-turn conversations", "AI performance degradation", "Microsoft Research", "Salesforce", "LLM unreliability", "reasoning models", "prompting strategies"]
summary: "Microsoft Research and Salesforce's paper shows top AI models drop from 90% to 65% performance in multi-turn conversations due to exploding unreliability from wrong assumptions and forgetting context, affecting even advanced models like o3 and DeepSeek R1. The recommended fix is to provide all information in a single upfront prompt instead of chatting back-and-forth."
quality_score: 8
quality_note: "Sensational tone but provides valuable insights into real-world AI limitations backed by research."
---

# Oliver Prompts
*Author: Oliver Prompts (@oliviscusAI)*
*URL: https://x.com/oliviscusAI/status/2030237913724645449*

Microsoft Research + Salesforce 刚刚发布了一篇论文，这应该让每一个 AI 构建者现在都感到害怕。他们在超过 200,000 次模拟对话中测试了 15 个顶级模型（GPT-4.1、Gemini 2.5 Pro、Claude 3.7 Sonnet、o3、DeepSeek R1、Llama 4）。结果实际上令人恐惧。如果你给模型一个单轮提示，它能达到 90% 的性能。但如果进行多轮对话？性能暴跌至 65%。同一个模型。同样的任务。只是……正常对话而已。疯狂的是，AI 并没有变笨（能力仅下降 15%），问题是不可靠性爆炸式增长了 112%……以下是它们崩溃的确切原因：→ 在你解释完之前就回答，那些错误的假设被永久固化 → 它们爱上自己的第一个错误答案，然后不断在其基础上构建 → 它们完全忘记了对话的中间部分 → 更长的响应引入更多假设，从而意味着更多错误即使是新的推理模型也失败了。o3 和 DeepSeek R1 的表现同样糟糕。给它们额外的“thinking tokens”完全没用。将 temperature 设置为 0？仍然崩溃。我们庆祝的每一个基准都在完美的、单提示实验室条件下测试。但真实对话会让市面上每一个模型都崩溃，而没人谈论这个……目前唯一的修复方法？停止聊天。在一条巨大的消息中一次性给出所有信息，而不是来回对话。

[![Image 1: Image](./assets/05_multi_turn_llm_conversations_degrade_performance_by_25/image-01.jpg)](https://x.com/oliviscusAI/status/2030237913724645449/photo/1)