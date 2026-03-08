---
title: "AI Models Fail in Real Conversations: Microsoft & Salesforce Study Exposes 25% Drop"
keywords: ["multi-turn conversations", "AI performance degradation", "Microsoft Research", "Salesforce", "LLM unreliability", "reasoning models"]
summary: "A Microsoft Research and Salesforce paper shows top AI models like GPT-4.1 and Claude 3.7 Sonnet drop from 90% to 65% performance in multi-turn conversations due to exploding unreliability from wrong assumptions and context forgetting. The workaround is providing all info in a single upfront prompt."
quality_score: 8
quality_note: "Insightful summary of recent AI research with clear explanations and practical advice."
---

# Oliver Prompts
*作者：Oliver Prompts (@oliviscusAI)*
*来源：https://x.com/oliviscusAI/status/2030237913724645449*

微软研究 + Salesforce 刚刚发布了一篇论文，这应该让每一个 AI 构建者现在都感到恐惧。他们测试了 15 款顶级模型（GPT-4.1、Gemini 2.5 Pro、Claude 3.7 Sonnet、o3、DeepSeek R1、Llama 4），跨越 200,000+ 次模拟对话。结果实际上令人恐惧。如果你给模型一个单轮提示，它能达到 90% 的性能。但如果进行多轮对话？性能暴跌至 65%。同样的模型。同样的任务。只是……正常对话而已。最疯狂的是，AI 并没有变笨（能力仅下降 15%）。问题是不可靠性爆炸式增长了 112%.. 它们崩溃的确切原因如下：→ 在你解释完之前就回答，那些错误的假设被永久固化 → 它们迷恋上自己的第一个错误答案，并不断在其基础上构建 → 它们完全忘记了对话的中间部分 → 更长的响应引入更多假设，这意味着更多错误即使是新的推理模型也失败了。o3 和 deepseek r1 表现同样糟糕。给予它们额外的“thinking tokens”完全没有作用。将 temperature 设置为 0？仍然崩溃。我们庆祝的每一个基准测试都是在完美的、单提示实验室条件下进行的。但真实对话会让市面上每一个模型崩溃，而没人谈论这一点.. 目前唯一的修复方法？停止聊天。与其来回对话，不如在一条巨型消息中一次性给你的 AI 所有信息。

[![图片 1：图片](./assets/05_multi_turn_llm_conversations_degrade_performance_by_25/image-01.jpg)](https://x.com/oliviscusAI/status/2030237913724645449/photo/1)