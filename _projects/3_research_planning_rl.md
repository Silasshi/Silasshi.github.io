---
layout: page
title: Training LLMs for Scientific Research Planning
description: Rubric-based RL for an open-ended task without verifiable reward.
importance: 3
category: research
github: https://github.com/Silasshi/co-scientist-rl
---

**Torr Vision Group, University of Oxford** · [code](https://github.com/Silasshi/co-scientist-rl)

**Motivation.** Research plans have no verifiable reward, so we use rubrics to make this open-ended task trainable, following the [ResearchPlanGen](https://arxiv.org/abs/2512.23707) dataset.

**Method.** I reproduced their results without released code by refining the rubric reward into a continuous score. Besides GRPO, I also implemented evolving rubrics ([DR Tulu](https://arxiv.org/abs/2511.19399)), self-distillation from grader and reviewer feedback ([SDPO](https://arxiv.org/abs/2601.20802)), and test-time training that reuses past attempts ([TTT-Discover](https://arxiv.org/abs/2601.16175)).

**Finding.** None of these methods brought a clear improvement over the reproduction. In our experiments, the rubric reward was easily hacked and too coarse to convey deep scientific content, so the policy mainly learned format and pattern preferences.
