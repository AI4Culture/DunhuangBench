# Dunhuang-Bench: How Well Do MLLMs Understand Cultural Heritage?

[![Paper](https://img.shields.io/badge/Paper-PDF-red.svg)](#)
[![Dataset](https://img.shields.io/badge/Dataset-Dunhuang--Bench-blue.svg)](#)

This repository contains the data and code for **Dunhuang-Bench**, the first large-scale, theory-grounded multimodal benchmark designed to evaluate how well Multimodal Large Language Models (MLLMs) understand Dunhuang art. 

## 📖 Overview

Dunhuang art, originating from the Mogao Caves and related grotto sites, stands as a quintessential representative of global cultural heritage. While MLLMs have shown strong performance on generic multimodal benchmarks, their capabilities in understanding culturally grounded artifacts remain largely unevaluated due to data scarcity and high annotation costs.

To bridge this gap, we introduce **Dunhuang-Bench**, a comprehensive dataset comprising **486 images and 22,970 QA pairs** sourced from the authoritative *Dunhuang Art Dictionary* and *Dunhuang Studies Dictionary*.

## ✨ Key Features

* **Theory-Grounded:** The benchmark's design is strictly guided by art-historical theories, specifically Panofsky's theory of iconology and the formal analytic tradition.
* **Diverse Task Formats:** It moves beyond simple multiple-choice questions by evaluating models across three distinct formats: Question Answering with Text Description (QA-T), Multi-turn Dialogue, and Question Answering with Choices (QA-C).
* **Large Scale:** It is currently the largest theory-grounded benchmark in this field, offering nearly tenfold the data of previous cultural VQA datasets.

## 🗂️ Task Structure

Dunhuang-Bench evaluates MLLMs across three hierarchical tasks to test different levels of cultural and visual understanding:

1. **Task 1: Visual Perception (QA-T)**
   * **Goal:** Evaluates the recognition of objective visual attributes through single-turn, image-based questions.
   * **Dimensions:** Counting, Color, Direction, and Behavior Recognition.
2. **Task 2: Knowledge Reasoning (Multi-turn Dialogue)**
   * **Goal:** Assesses the model's ability to progressively integrate visual evidence with expert cultural knowledge across a 4-turn dialogue.
   * **Dimensions:** Basic Info, Cultural Elements, Specific Details, and Deeper Meaning.
3. **Task 3: Artistic Appreciation (QA-C)**
   * **Goal:** Measures the capability to discriminate fine-grained stylistic differences in a multiple-choice setting.
   * **Dimensions:** Composition and Layout, Color Usage, and Form and Style.

## 📊 Key Findings

We extensively evaluated 20 mainstream closed-source (e.g., Gemini 2.5, GPT-5.1) and open-source (e.g., InternVL, Qwen-VL) MLLMs.

* **Current Limitations:** MLLMs face fundamental challenges in performing cultural understanding in Dunhuang art. The top-performing model (InternVL3.5-241B-A28B) achieved an average score of only 50.9%.
* **Task Difficulty:** There is a consistent performance drop from basic visual perception to multi-turn knowledge reasoning.
* **Prompting Shortfalls:** Standard reasoning techniques like Chain-of-Thought (CoT) and few-shot prompting exhibited marginal or even negative impacts on performance, highlighting the limits of prompting-based improvements without strong visual grounding.
* 
## 📑 Access Protocol

To access the dataset, please:  
1. **Fill in the Data Usage Agreement Form** [![Agreement](https://img.shields.io/badge/Agreement-Form-blue)](https://github.com/AI4Culture/DunhuangBench/blob/main/Application-Form.docx)
2. After review, you will receive the **password** via email.  
3. Use the password to unzip the dataset files.

## ✒️ Citation

If you find our data or work useful, please consider citing our paper:

```bibtex
@inproceedings{yuan2026dunhuangbench,
  title={Dunhuang-Bench: How Well Do MLLMs Understand Cultural Heritage?},
  author={Yuan, Junyi and Zhang, Jian and Yu, Tianxiu and Zhou, Yanlin and Jin, Xiaobo and Wang, Qiufeng and Wu, Fangyu},
  booktitle={Findings of the 64th Annual Meeting of the Association for Computational Linguistics (ACL)},
  year={2026}
}
