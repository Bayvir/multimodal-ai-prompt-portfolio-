# Multimodal & Visual AI Prompt Evaluation Portfolio
**Curator:** Jide Thompson | Linguist & Certified AI Specialist

## Overview
A comparative benchmarking framework for evaluating and fine-tuning text-to-image (Midjourney/DALL-E) and text-to-video (Sora/Runway) generative AI models. Focuses on spatial accuracy, frame consistency, negative constraint adherence, and camera directive precision.

---

## 1. Text-to-Image (T2I) Spatial & Compositional Evaluation

| Baseline Prompt | Target Output / Intent | Model Output Defect | Model Failure Mode | Optimized Prompt / Fix | Evaluation Verdict |
| :--- | :--- | :--- | :--- | :--- | :--- |
| *"A glass cup on a wooden table to the left of a open book."* | Clear spatial separation between objects. | Glass cup generated directly on top of the open book pages. | Spatial preposition misinterpretation ("to the left of"). | *"A wooden table. On the right side sits an open book. Positioned separately on the far left side of the table is a clear glass cup."* | **PASS** — Correct spatial segregation achieved. |
| *"A portrait of a futuristic pilot wearing zero silver jewelry."* | Complete absence of metallic accessories. | Subject rendered with silver earrings and a chrome neck collar. | Negative constraint leakage ("zero silver"). | *"A minimalist portrait of a futuristic pilot. Attire: plain fabric jumpsuit. Strictly omit all jewelry, necklaces, earrings, and metallic ornaments."* | **PASS** — Negative constraints fully respected. |

---

## 2. Text-to-Video (T2V) Temporal & Camera Motion Benchmarking

| Baseline Directive | Camera & Motion Expectations | Observed Defect | Temporal Failure Mode | Optimized Prompting Strategy |
| :--- | :--- | :--- | :--- | :--- |
| *"A slow tracking shot following a running dog through a field."* | 5-second continuous motion, 35mm lens tracking, steady focal depth. | Subject limbs distorted at 00:03; background blurred artificially. | Motion coherence degradation across extended keyframes. | *"35mm cinematic tracking shot: A golden retriever runs smoothly across a grassy field. Camera maintains parallel panning speed. Zero blur, constant focal depth."* |
| *"A drone shot ascending smoothly over a coastal cliff."* | Vertical upward camera trajectory without horizontal jitter. | Camera angle flipped inverted mid-flight at frame 60. | Spatial orientation loss in multi-axis movement. | *"Aerial drone footage: Straight vertical ascend vector above a coastal cliff. High-angle perspective, smooth upward elevation, static tilt angle."* |

---

## Guidelines for Visual Prompt Annotators
1. **Isolate Variables:** Test prepositional syntax separately from style/lighting directives.
2. **Track Keyframe Drift:** In T2V evaluations, flag object morphing across 1-second intervals.
3. **Verify Negative Directives:** Confirm the model actively excludes prohibited elements rather than reducing their opacity.
