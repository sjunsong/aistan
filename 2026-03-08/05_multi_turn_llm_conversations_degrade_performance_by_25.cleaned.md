---
title: "Multi-Turn Conversations Plummet AI Performance by 25%: Microsoft & Salesforce Research"
keywords: ["multi-turn conversations", "AI performance", "Microsoft Research", "Salesforce", "LLM degradation", "prompt engineering", "reasoning models"]
summary: "Microsoft Research and Salesforce tested top AI models in 200,000+ simulated conversations, finding performance drops from 90% in single-turn prompts to 65% in multi-turn due to exploding unreliability from wrong assumptions and context forgetting. The fix is to provide all info in one upfront prompt instead of chatting back-and-forth."
quality_score: 7
quality_note: "Sensationalized language but provides a clear, informative summary of key research findings with practical advice."
---

# Oliver Prompts
*Author: Oliver Prompts (@oliviscusAI)*
*URL: https://x.com/oliviscusAI/status/2030237913724645449*

Microsoft Research + Salesforce just dropped a paper that should scare every single AI builder right now. They tested 15 of the top models (GPT-4.1, Gemini 2.5 Pro, Claude 3.7 Sonnet, o3, DeepSeek R1, Llama 4) across 200,000+ simulated conversations. The results are actually terrifying. If you give a model a single-turn prompt, it hits 90% performance. But if you have a multi-turn conversation? it plummets to 65%. same model. same task. just.. talking normally. The crazy part is that the ai isn't getting dumber (aptitude only dropped 15%). the problem is that unreliability EXPLODED by 112%.. Here is exactly why they break: → they answer before you finish explaining, and those wrong assumptions get baked in permanently → they fall in love with their first wrong answer and just keep building on it → they completely forget the middle of your conversation → longer responses introduce more assumptions, which means more errors Even the new reasoning models failed. o3 and deepseek r1 performed just as badly. giving them extra "thinking tokens" did absolutely nothing. setting temperature to 0? still broken. Every benchmark we celebrate is tested in perfect, single-prompt lab conditions. but real conversations break every model on the market and nobody is talking about it.. The only fix right now? stop chatting. Give your AI everything upfront in one massive message instead of going back-and-forth.

[![Image 1: Image](./assets/05_multi_turn_llm_conversations_degrade_performance_by_25/image-01.jpg)](https://x.com/oliviscusAI/status/2030237913724645449/photo/1)