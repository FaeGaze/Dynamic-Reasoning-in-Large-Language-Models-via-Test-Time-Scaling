# Simple Test-Time Scaling for Improved LLM Reasoning
### Paper: "Simple Test-Time Scaling: Improving Reasoning by Spending More Time at Test-Time" – DeepSeek-AI

## Overview
This research explores enhancing reasoning in large language models (LLMs) not by retraining, but by increasing the "thinking time" at inference. It introduces a technique called **Budget Forcing**, allowing LLMs to perform more deliberate, structured reasoning during test time. 

## Motivation
- Traditional LLMs are static post-training and cannot adapt or improve without fine-tuning.
- Complex tasks (e.g., AIME math, science QA) require stepwise, logical reasoning.
- Inspired by OpenAI’s o1 model, but with a fully open-source alternative: **s1-32B**.

## Key Contributions
- **s1-32B**, a 32B-parameter reasoning-optimized LLM, trained on only **1,000 curated examples**.
- **Budget Forcing**: A novel method for controlling test-time compute (e.g., using prompts like “Wait”).
- **REBASE**: A reward-based inference mechanism that scores multiple reasoning paths and picks the best one.
- Demonstrated performance rivaling models trained on **800K+ examples**.
- Introduced evaluation metrics: **Control**, **Scaling**, **Performance**.

## Results
- Outperforms traditional prompting on tasks like GPQA, MATH500, AIME24.
- "Wait" prompting yields up to **53.3% accuracy** on AIME24.
- REBASE pushes test-time performance even further, especially for logic-heavy tasks.

## Practical Insights
- Open-weights: Anyone can run s1-32B (with ~60GB VRAM or via quantized models).
- Accessible to researchers via Hugging Face, Colab, and Replicate.
- Great tool for studying reasoning with minimal compute.

## Conclusion
**Test-time scaling** is a practical, efficient path toward better LLM reasoning without the cost of retraining. Techniques like Budget Forcing and REBASE open the door to flexible and controllable inference for high-stakes tasks.

## Video Presentation
[Watch on YouTube](https://www.youtube.com/watch?v=vvnL_W2bKBU&t=524s)
