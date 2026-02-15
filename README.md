#TNM Cancer Staging with Large Language Models
Comparative Analysis of MedPrompt and Other Structured Prompting Techniques

This repository contains the official preprint of the research article:

"TNM Cancer Staging with Large Language Models: Comparative Analysis of MedPrompt and Other Structured Prompting Techniques"

📄 Full paper (PDF):
https://drive.google.com/file/d/1Vn0Wi5Ps_6zmOqlpQQFmUS-IEIO3Q7wG/view

📌 Abstract

TNM cancer staging is essential for assessing cancer severity, guiding treatment decisions, and predicting clinical outcomes. Although Large Language Models (LLMs) show promise in automating TNM staging, their clinical reliability depends on strict adherence to oncological guidelines.

This study evaluates three LLMs:

GPT-4o mini

LLaMA 3.3 70B Instruct

DeepSeek-R1-Distill-LLaMA-70B

Across 1,000 TCGA pathology reports spanning 33 cancer types, we compare:

Zero-Shot

Zero-Shot + Chain-of-Thought

MedPrompt

Approach A: Self-generated rule-based structured reasoning

Approach B: AJCC-guideline-integrated structured reasoning

Key Results

Approach B achieved state-of-the-art performance

N Macro Average Precision: 0.88

M Macro Average Precision: 0.91

MedPrompt achieved the highest overall TNM macro average precision

Mean Macro Precision: 0.867

Our findings highlight the critical role of domain-specific structured prompting in improving LLM accuracy, reducing hallucinations, and increasing clinical reliability in automated TNM staging.

🧠 Research Contributions

Introduction of two structured inference frameworks for TNM classification

Explicit integration of AJCC 8th edition rules

Replication of pathologist reasoning workflow inside LLM inference

Comparative evaluation of advanced prompting methodologies

Systematic T, N, and M separated macro-average evaluation

Analysis of reasoning scaffolding effects on LLM clinical reliability

📊 Dataset

1,000 pathology reports

Extracted from TCGA

33 cancer types

Pathological TNM staging

🔬 Methodology Overview
Approach A

Few-shot + Cancer Location + Self-Generated Staging Rules + Chain-of-Thought

Approach B

Cancer Location Classification + Structured T/N/M Decomposition + Explicit AJCC Integration + Chain-of-Thought

🎯 Keywords

Large Language Models, Cancer Staging, TNM, AJCC, MedPrompt, Chain-of-Thought, Clinical NLP, Medical AI, Prompt Engineering

📚 Citation

If you find this work useful, please cite:

Rodrigo Stall.
TNM Cancer Staging with Large Language Models: Comparative Analysis of MedPrompt and Other Structured Prompting Techniques.
2026.

📩 Contact

Rodrigo Stall
AI Researcher – Medical AI & LLM Systems
