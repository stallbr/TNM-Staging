## 📊 TNM Cancer Staging Using LLMs and Innovative Prompting Techniques

This repository contains the official preprint of the research article:

"TNM Cancer Staging with Large Language Models: Comparative Analysis of MedPrompt and Other Structured Prompting Techniques"

📌 Abstract

TNM cancer staging is essential for assessing cancer severity, guiding treatment decisions, and predicting clinical outcomes. 
This standardized system allows healthcare professionals to assess tumor progression and tailor treatment strategies accordingly.
Although large language models (LLMs) show promise in automating TNM staging, their clinical reliability depends on strict ad-
herence to oncological guidelines. This study evaluates the performance of three LLMs—GPT-4-o mini, LLaMA 3.3 70B Instruct,
and DeepSeek-R1-Distill-LLaMA-70B—in classifying TNM stages across 1,000 TCGA pathology reports from 33 cancer types.
We compare traditional prompting techniques, including Zero-Shot and Zero-Shot with Chain-of-Thought, with the specialized
MedPrompt and two novel methodologies: Approach A, which mimics the step-by-step reasoning process of medical profession-
als using self-generated staging rules, and Approach B, which follows the same structured process while explicitly integrating
AJCC guidelines. Our findings show that Approach B achieved state-of-the-art results in the N and M categories, with N macro
average precision reaching 0.88 and M macro average precision reaching 0.91. Additionally, MedPrompt achieved the highest
mean macro average precision across the three TNM categories, with a score of 0.867. These findings highlight the critical role of
domain-specific structured prompting in improving LLM accuracy, minimizing hallucinations, and ensuring clinical reliability in
automated TNM cancer staging.

## 📊 Model Architecture

## 🧠 Approach B – AJCC-Guided Structured TNM Framework

In this approach, we replicate the steps typically used by oncologists for TNM cancer staging, similar to Approach A, but with a key distinction:

Instead of generating the AJCC Classification Staging Rules, we provide them directly to the model.

This ensures stricter control over the staging criteria and significantly reduces hallucination risks.

Additionally, the LLM is instructed to:
- Summarize the clinical case
- Identify tumor size
- Reason through each TNM component
- Generate a structured Chain-of-Thought
- Assign final TNM classifications

---

### 🔎 Structured Workflow

#### 1️⃣ Cancer Category Classification
A dedicated LLM classifier first identifies the cancer location based on AJCC Cancer Staging Manual categories.

#### 2️⃣ Staging Rules Input
Once the cancer type is identified, the corresponding AJCC staging rules are explicitly provided to the model.

This guarantees:
- Strict rule adherence  
- Controlled decision boundaries  
- Reduced hallucinations compared to self-generated rule strategies  

#### 3️⃣ Few-Shot Examples Input
Cancer-specific few-shot examples are included to guide reasoning and illustrate correct staging decisions.

---

### 🏥 Clinical Case Analysis Pipeline

The LLM performs the following structured steps:

1. Generate a summary of the clinical case  
2. Identify tumor size  
3. Provide reasoning for the **T stage** classification  
4. Provide reasoning for the **N stage** classification  
5. Provide reasoning for the **M stage** classification  
6. Generate a self-guided Chain-of-Thought  
7. Assign the final **T classification**  
8. Assign the final **N classification**  
9. Assign the final **M classification**

---

This structured decomposition mirrors real-world oncological reasoning while maintaining full alignment with AJCC guidelines.


<p align="center">
  <img src="approach_b.png" width="700">
</p>


📩 Contact

Rodrigo Stall

rodrigo.stall.sikora@gmail.com

Data Scientist and Machine Learning Engineer
