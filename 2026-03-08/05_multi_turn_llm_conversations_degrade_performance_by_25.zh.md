---
title: "Top AI Models Fail in Real Conversations: Microsoft & Salesforce Paper Exposes 25% Performance Drop"
keywords: ["multi-turn conversations", "AI performance degradation", "Microsoft Research", "Salesforce", "LLM unreliability", "reasoning models", "single-turn prompts"]
summary: "Microsoft Research and Salesforce tested top AI models like GPT-4.1 and Claude 3.7 Sonnet, finding performance drops from 90% in single-turn prompts to 65% in multi-turn conversations due to exploding unreliability from wrong assumptions and forgetting context. The post advises providing all information upfront to avoid issues."
quality_score: 8
quality_note: "Engaging, informative summary of research findings with clear insights and practical advice; hype-y tone but backed by specifics."
---

# Oliver Prompts
*Author: Oliver Prompts (@oliviscusAI)*
*URL: https://x.com/oliviscusAI/status/2030237913724645449*
------------

微软研究 + Salesforce 刚刚发布了一篇论文，这应该让每一个 AI 构建者现在就感到恐惧。他们测试了 15 个顶级模型（GPT-4.1、Gemini 2.5 Pro、Claude 3.7 Sonnet、o3、DeepSeek R1、Llama 4），跨越 200,000+ 次模拟对话。结果实际上令人恐惧。如果你给模型一个单轮提示，它能达到 90% 的性能。但如果你进行多轮对话？性能暴跌至 65%。同一个模型。同一个任务。只是……正常对话而已。最疯狂的是，ai 并没有变笨（能力仅下降 15%）。问题是不可靠性爆炸式增长了 112%…… 它们崩溃的确切原因如下：→ 它们在你解释完之前就回答，那些错误的假设被永久固化 → 它们爱上了自己的第一个错误答案，并不断在其基础上构建 → 它们完全忘记了对话的中间部分 → 更长的响应引入了更多假设，从而意味着更多错误 即使是新的推理模型也失败了。o3 和 deepseek r1 的表现同样糟糕。给它们额外的“thinking tokens”完全没用。将 temperature 设置为 0？仍然崩溃。 我们庆祝的每一个基准测试都是在完美的单提示实验室条件下进行的。但真实对话会让市面上每一个模型崩溃，而没人谈论这件事…… 目前唯一的修复方法？停止聊天。一次性在一条长消息中给你的 AI 提供所有信息，而不是来回对话。

[![Image 1: Image](./assets/05_multi_turn_llm_conversations_degrade_performance_by_25/image-01.jpg)](https://x.com/oliviscusAI/status/2030237913724645449/photo/1)

读者添加了他们认为人们可能想知道的上下文

上下文由使用 X 的人撰写，并在被他人评为有用时显示。[了解更多](https://x.com/i/flow/join-birdwatch)。