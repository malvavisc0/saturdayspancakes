---
layout: post
title: "I hate AI Benchmarks, plain and simple"
description: "A rant on why leaderboard scores are failing us and what we should actually be measuring."
date: 2026-05-09
categories: ai
tags: [rants]
---

Let's face it: there is no escaping benchmarks. I know that. But the reality is that benchmarks are becoming meaningless. Every time a new model is released, benchmarks are attached like some kind of official certification. We download the model because, of course, the numbers look great—and then, after three or four runs, the model just crashes or loses its mind. It makes no sense. Do you really train a model, run the benchmarks, and then just... forget to actually test it? How is that possible? Unless, of course, the only thing that actually matters is hitting a high number to get views on social media.

Maybe the fault lies with social media; I suppose we've reached a point where we link value directly with virality. Regardless, I'd like to think that the people building AI actually want to *use* it. Or maybe I'm just wrong.

Take Gemma 4. I liked it from day one. It's a great model—solid with simple tasks, good at making decisions, and capable at writing. But it has a problem: it hallucinates subtly but frequently. That's a deal-breaker if you want to use it as an everyday driver. Then we have Qwen 3.6 and all its fine-tuned versions that supposedly "beat everybody." It's always the same script: someone releases a fine-tune, attaches a benchmark, and skips the actual testing. You see posts raving about how "super-duper smart" the model is because of the scores, so you download it, start using it, and then drop it after a few rounds because the model completely loses the plot the moment it has to use a few tools and handle a follow-up request.

In theory, AI benchmarks are the standardized rulers of the industry. Without them, we'd be left with nothing but marketing claims and cherry-picked examples. That is exactly what benchmarks were supposed to fix, but here we are in 2026, and we're just walking in circles. Because high scores drive investment and attention, developers are optimizing models specifically to pass the tests rather than improving underlying reasoning. We're seeing massive "benchmark leakage" (or data contamination), where the test questions end up in the training data. The model is just reciting memorized answers. When a model dominates something like SWE-bench, you're often looking at performance in a vacuum. Most benchmarks are stateless—one prompt, one output, one grade.

The industry needs to stop this "fake it until you make it" mentality. We need to start prioritizing "stamina" via Context Degradation benchmarks. We need to know: does the model stay coherent over a long conversation, or does its reasoning degrade after the fifth exchange? We also need to measure the "negatives." Instead of only asking, "Can the model solve this math problem?" we should be asking, "Can we trick the model into confidently lying?" or "Will it admit when it doesn't know the answer?"

I know there are people trying to solve this, but it's not gaining traction. Maybe the scene is too polluted with people chasing a quick buck, or maybe there just isn't enough talent focused on the right problems. In the meantime, **I'll keep blaming social media**. Until we stop treating single-number leaderboard scores as absolute proof of intelligence, there will always be a massive gap between the social media hype and the actual experience on your desktop.

"When a measure becomes a target, it ceases to be a good measure." — Charles Goodhart.