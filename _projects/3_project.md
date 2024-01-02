---
layout: page
title: Novel Object Detection in Autonomous Vehicles using Reasoning by Elimination
description:
img: /assets/img/object_detection.jpg
redirect:
importance: 3
category: Course Projects
---

# Autonomous Vehicle Object Detection Using Reinforcement Learning

## 🛠️ Tech Stack Used

- **Core Programming Language**: Python
- **Machine Learning Frameworks**: PyTorch, Reinforcement Learning, Proximal Policy Optimization (PPO)

---

## 📖 Introduction

- **Concept**: Developing an innovative object detection system for autonomous vehicles using a reasoning by elimination approach.
- **Objective**: Enhance the reliability and efficiency of autonomous vehicle perception systems in various environments.

## 📊 Dataset

- **Icon Image Dataset (Nounproject)**: Custom dataset of 6000 images in 20 classes with 6 color variations, using icons from ‘The Noun Project’.
- **Real World Image Dataset**: Generated using Stable Diffusion XL base-1.0 with HuggingFace, focusing on 7 classes colored in 6 different shades, totaling 1260 images.
- **Test Dataset**: Includes unseen classes and colors to evaluate the model's adaptability.
- **Dataset Quality Assessment**: Employed 'Everypixel' API for aesthetic scoring and quality assurance.

## 🔍 Methodology

- Worked as a group on this project
- **Perception Model Development**: Used ResNet and BERT frameworks to train perception module .
- Embeds an object’s visual appearance along with its textual description in a single multi-modal space. By using symmetric contrastive loss, the two mappings are learned by maximising the cosine-similarity between the visual and textual feature vectors.
- **Custom Dataset Creation**: Generated 2000 images using Stable Diffusion SDXL, specifically focusing on cars and other road objects.
- **Reasoning Model with PPO**: Developed a custom policy network with Proximal Policy Optimization for efficient object identification.

## 📈 Results

### Reasoning Module Performance

- **Seen and Unseen Object Recognition**:
  - The RL agent demonstrated notable efficiency in identifying both seen and unseen objects.
  - **Seen Accuracy**: Achieved 92% (±1.26) on the Nounproject dataset, outperforming the baseline of 88% (±3.24).
  - **Unseen Accuracy**: Comparable results with 65% (±3.15) against the baseline's 67% (±4.72).

### Comparative Analysis

- **Nounproject Dataset**:

  - Our approach showed superior performance on seen objects and comparable results on unseen objects.

- **Real World Dataset**:
  - **Seen Accuracy**: Recorded at 86% (±1.24), demonstrating robustness in complex real-world scenarios.
  - **Unseen Accuracy**: Maintained at 65% (±3.18), indicating effective generalization capabilities.

### Ablation Study

- **Single Object Task with Different Features**:
  - **Using Only Similarity Scores**:
    - Seen: Improved from 88% (±3.24) baseline to 93% (±2.26) with our model.
    - Unseen: Slight improvement from 67% (±4.72) baseline to 68% (±3.15).
  - **Similarity Scores + Top1 Scores**:
    - Seen: 92% (±1.37) with our approach compared to 87% (±3.36) baseline.
    - Unseen: Our model's 78% (±3.79) closely follows the baseline's 79% (±4.01).
  - **All Features Combined**:
    - Our method achieved near parity with the baseline, with both scoring around 87% for unseen accuracy.

---

<!-- ## 🖼️ Visualizations

- **Dataset Samples**: Showcase the variety and complexity of the dataset images, including icon-based and real-world scenarios.
- **Model Performance Charts**: Graphs depicting the accuracy and efficiency of the Perception and Reasoning Models under various conditions.
- **Comparative Analysis**: Visual comparisons between standard object detection models and the newly developed model, emphasizing improvements.

---
-->
