# Artificial Intelligence for Security  
## Group Assignment – Academic Year 2025/26

**Course:** Artificial Intelligence for Security  
**Assignment Type:** Group Project  

---

## 📌 Project Overview

This project was developed as part of the *Artificial Intelligence for Security* course (AY 2025/26).  
The goal of the assignment is to analyse a large, real-world cybersecurity dataset and apply **data analysis, visualization, and machine learning techniques** to extract meaningful security-related insights.

The work is implemented in a **self-contained Python notebook**, designed to clearly explain:
- the data exploration process,
- the applied methodologies,
- the obtained results, and
- the conclusions drawn from the analysis.

---

## 📂 Selected Dataset

For this assignment, we selected the following dataset:

**Dataset of Jailbreak Attacks on Large Language Models (LLMs)**  
📎 https://huggingface.co/datasets/qualifire/prompt-injections-benchmark

This dataset contains:
- **benign prompts**, and
- **malicious prompts** specifically designed to perform *prompt injection* and *jailbreak attacks* on LLMs.

The dataset represents a realistic and emerging cybersecurity threat, making it highly relevant to the scope of AI security.

---

## 🎯 Objectives

The main objectives of this project are to:

- Explore and understand the structure and characteristics of a real cybersecurity dataset
- Identify patterns that distinguish malicious prompts from benign ones
- Apply **supervised and unsupervised machine learning techniques**
- Investigate **anomaly detection** approaches
- Critically interpret the results in a cybersecurity context

---

## 🧪 Methodology

The analysis follows the structure suggested in the assignment description and is adapted to the textual and security-oriented nature of the selected dataset, which consists of benign and malicious prompts targeting Large Language Models (LLMs).

### A) Summary Statistics and Data Exploration
We begin with an exploratory analysis of the dataset, focusing on:
- the number of samples and overall dataset structure
- the distribution of benign versus jailbreak (malicious) prompts
- basic statistics related to prompt length and textual characteristics

This step provides initial insights into class balance and the nature of malicious prompts.

### B) Text Analysis and Visualization
Given the textual nature of the data, we perform:
- keyword-based analysis using a manually defined blacklist of suspicious terms
- qualitative inspection of prompt content
- dimensionality reduction and visualization (t-SNE) applied to text embeddings to analyse separability between benign and malicious prompts

### C) Text Representation (Embeddings)
Prompts are converted into numerical representations using multiple embedding strategies:
- **Word-level embeddings**: Word2Vec, GloVe, FastText
- **Sentence-level embeddings**: Sentence-BERT
- variants with and without stemming
- vector normalization

These representations are compared to assess their impact on downstream learning tasks.

### D) Supervised Learning
Using the extracted embeddings, we train and evaluate several supervised classifiers:
- Logistic Regression
- Naive Bayes
- Support Vector Machines (linear and kernel-based)
- Decision Tree
- Random Forest
- XGBoost
- k-Nearest Neighbors (k-NN)
- Neural Network classifiers

Models are compared using appropriate evaluation metrics to identify the most effective approaches for jailbreak detection.

### E) Clustering (Unsupervised Learning)
To explore the intrinsic structure of the data without using labels, we apply multiple clustering techniques:
- k-Means
- Agglomerative Clustering
- DBSCAN

Clusters are visualized using dimensionality reduction techniques and analysed to determine whether they correspond to meaningful groupings of prompts or distinct jailbreak behaviours.

### F) Anomaly Detection
We apply anomaly detection methods to identify unusual or potentially malicious prompts:
- One-Class SVM
- Isolation Forest
- Local Outlier Factor (LOF)

Detected outliers are analysed to assess whether they represent genuine jailbreak attempts or noise.

### G) LLM-Based Analysis
In addition to classical machine learning methods, we include a compact **LLM-based classification** experiment as a reference baseline.

The LLM is prompted to assess whether a given input constitutes a jailbreak attempt. Its predictions are compared with ground-truth labels and with the results obtained using traditional ML models.

### H) Comparative Analysis and Discussion
Across all experiments, we perform a comparative analysis focusing on:
- differences in performance across models and embeddings
- robustness and interpretability in a cybersecurity context
- strengths and limitations of supervised, unsupervised, and LLM-based approaches

### I) Further Considerations
We conclude by discussing potential extensions, including:
- end-to-end deep learning approaches
- real-time prompt filtering systems
- evaluation on additional or larger prompt injection datasets

