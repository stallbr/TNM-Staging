# 📊 TNM Cancer Staging with Large Language Models  

This repository contains the official preprint and methodological details for:

**TNM Cancer Staging with Large Language Models: Comparative Analysis of MedPrompt and Other Structured Prompting Techniques**
**Authors:** Rodrigo Stall, Gabriel Lino Garcia, João Paulo Papa  

📄 **Preprint PDF:** [Download Full Paper (PDF)](https://raw.githubusercontent.com/stallbr/TNM-Staging/main/TNMCancer%20Staging%20with%20Large%20Language%20Models_%20Comparative%20Analysis%20of%20MedPrompt%20%20and%20Other%20Structured%20Prompting%20Techniques.pdf)

---

## 📌 Abstract

TNM cancer staging is essential for assessing cancer severity, guiding treatment decisions, and predicting clinical outcomes. This standardized system enables clinicians to evaluate tumor progression and determine appropriate therapeutic strategies.

Although Large Language Models (LLMs) show promise in automating TNM staging, their clinical reliability depends on strict adherence to oncological guidelines. This study evaluates the performance of three LLMs—GPT-4o-mini, LLaMA 3.3 70B Instruct, and DeepSeek-R1-Distill-LLaMA-70B—in classifying TNM stages across 1,000 TCGA pathology reports spanning 33 cancer types.

We compare traditional prompting strategies (Zero-Shot and Zero-Shot with Chain-of-Thought) with:

- **MedPrompt**
- **Approach A** – Self-Generated AJCC Rule Framework
- **Approach B** – AJCC-Guided Structured Framework

Our findings highlight the critical role of domain-specific structured prompting in improving LLM accuracy, minimizing hallucinations, and ensuring clinical reliability in automated TNM cancer staging.

---

# 📑 Repository Overview

- 🧠 MedPrompt Framework  
- 🧠 Approach A – Self-Generated Rule Strategy  
- 🧠 Approach B – AJCC-Guided Structured Strategy  
- 📊 Experimental Setup  
- 📈 Results (To Be Updated)  
- 📩 Contact  

---

# 🧠 MedPrompt – Advanced Structured Prompting for Medical AI

<p align="center">
  <img src="Medprompt.png" width="800">
</p>

MedPrompt is an advanced prompting framework designed to enhance the performance of LLMs in medical reasoning tasks.

It integrates multiple state-of-the-art techniques:

- K-Nearest Neighbors (KNN)
- Few-Shot Learning
- Self-Generated Chain-of-Thought
- Self-Consistency Aggregation

### 🔎 Core Mechanism

#### 1️⃣ Contextual Example Retrieval (KNN)
Relevant examples are retrieved using similarity-based selection and embedded directly into the prompt to provide contextual grounding.

#### 2️⃣ Structured Reasoning (Chain-of-Thought)
The model generates step-by-step reasoning to improve interpretability and logical coherence.

#### 3️⃣ Self-Consistency
Multiple candidate outputs are generated and aggregated to select the most consistent prediction, reducing variability and hallucination risk.

---

### 🔀 Options Shuffling Strategy

MedPrompt incorporates a dynamic options shuffling mechanism that alters answer ordering to mitigate positional bias and encourage deeper reasoning.

This is particularly beneficial for complex clinical classification tasks.

---

# 🧠 Approach A – Self-Generated AJCC Rule Framework

<p align="center">
  <img src="Approach A.png" width="800">
</p>

Approach A replicates the structured reasoning process typically followed by oncologists when assigning TNM classifications.

### 🔎 Workflow

1. **Cancer Location Identification**
2. **Self-Generation of AJCC Staging Rules**
3. **Structured Chain-of-Thought Reasoning**
4. **Final TNM Classification (T, N, M)**

This strategy relies exclusively on the model’s internal knowledge to reconstruct AJCC criteria without external rule injection.

The goal is to simulate expert clinical reasoning under constrained prompting.

---

# 🧠 Approach B – AJCC-Guided Structured TNM Framework

<p align="center">
  <img src="Approach B.png" width="800">
</p>

Approach B follows a similar sequential reasoning structure as Approach A but explicitly injects official AJCC staging rules into the prompt.

### 🔎 Workflow

1. **Cancer Type Classification**
2. **Explicit AJCC Rule Injection**
3. **Few-Shot Example Conditioning**
4. **Structured Clinical Decomposition**
5. **Chain-of-Thought Reasoning**
6. **Final TNM Assignment**

### 🏥 Clinical Decomposition Pipeline

The model is instructed to:

- Generate a structured summary of the clinical case
- Identify tumor size and relevant factors
- Reason independently for T, N, and M categories
- Produce a self-guided reasoning trace
- Assign final TNM classifications

This methodology enforces strict guideline adherence while preserving interpretability and decision transparency.

---

# 📊 Experimental Setup

- **Dataset:** 1,000 TCGA pathology reports  
- **Cancer Types:** 33 distinct tumor locations  
- **Models Evaluated:**
  - GPT-4o-mini
  - LLaMA 3.3 70B Instruct
  - DeepSeek-R1-Distill-LLaMA-70B
- **Evaluation Metric:** Macro Average Precision per TNM category  

All experiments were conducted under controlled prompting configurations to ensure methodological fairness across strategies.

---

# 📈 Results

🚧 *Results section will be updated with full quantitative comparison tables.*

This section will include:

- Macro Average Precision per TNM component (T, N, M)
- Mean Macro Average
- Comparative performance across prompting strategies
- Error analysis and hallucination rate comparison

---

# 📩 Contact

**Rodrigo Stall**  

📧 rodrigo.stall.sikora@gmail.com  

Data Scientist | Machine Learning Engineer
