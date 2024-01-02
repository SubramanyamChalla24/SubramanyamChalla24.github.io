---
layout: page
title: AdPrompter - Reinforcement Learning for Persuasive Ads
description:
img: /assets/img/kfc_img.jpeg
importance:
category: Course Projects
---

## 🛠️ Project Overview

- **Goal**: Develop a comprehensive system for creating persuasive advertisements working in a group.
- **Tech Stack**: Python, PyTorch, Reinforcement Learning, Stable Diffusion XL, Large Language Models

---

## 📖 Introduction

- **Objective**: To create an innovative ad generation model employing persuasive strategies, enhancing ad relevance and engagement.
- **Approach**: Utilize a mix of advanced NLP and image generation techniques, combined with reinforcement learning.

## 📊 Dataset

- **Sources**: Custom prompts, human feedback, and images generated using Stable Diffusion XL.
- **Target Companies**: H&M, Coca-Cola, KFC.
- **Dataset Details**: Images rated for their effectiveness in ad campaigns for the specified companies.

## 🔍 Methodology

### 3.1 Prompt Generation

- **LLM Fine-tuning**: Enhanced general LLMs to generate text-2-image prompts, particularly for ad creation.
- **Model Selection**: Chose GPT-2 trained with Stable-diffusion datasets for optimal performance.
- **Prompt Format**: “Make a convincing ad for [Company] including themes of [Strategy]”.

### 3.2 Text-2-Image Generation

- **Model Experimentation**: Tested various models including DALL-E and Midjourney, before selecting Stable Diffusion XL.
- **Iterative Improvement**: Continuously refined using human feedback to align images with strategic ad goals.

### 3.3 RL Model-1

- **Algorithm Choice**: Selected Proximal Policy Optimization (PPO) for its sample efficiency and policy gradient method.
- **Training**: Conducted over 200 episodes and 512k timesteps, focusing on strategy exploration for ad generation.

### 3.4 Human Feedback

- **Evaluation Method**: Ads rated on quality and strategy incorporation, with scores of 0, 5, or 10.
- **Reliability Check**: Cohen’s Kappa statistic used to ensure consistent and reliable feedback.

### 3.5 Model-2

- **Bias Detection**: Implemented a bias detection model from Hugging Face to classify prompts as biased or non-biased.

## 📈 Results

- **Ad Prompt Generation**: Achieved a 60% increase in application of persuasive strategies.
- **Image Generation**: Produced over 5,000 optimized images for ad campaigns.
- **Reinforcement Learning Efficiency**: Improved strategy selection accuracy by 40%.

<!-- ## 🖼️ Visualizations

- **Ad Samples**: Showcase the range of ads created for the target companies.
- **Performance Metrics**: Graphs and charts depicting the success rates of various strategies and models.
- **Bias Analysis**: Visual representation of bias detection results.

--- -->
