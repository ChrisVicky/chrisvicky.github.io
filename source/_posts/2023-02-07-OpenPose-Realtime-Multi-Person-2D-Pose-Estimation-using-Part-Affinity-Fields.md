---
layout: paperreview
title: 'Paper Review: OpenPose: Realtime Multi-Person 2D Pose Estimation using Part Affinity Fields'
categories:
    - PaperReview
cover: /myimg/OpenPose-Architecture.png
date: 2023-02-07 12:28:41
tags:
    - PaperReview
    - OpenPose
    - Pose Estimation
    - PAF
    - AI
    - ML
---

<center>
  <img style="border-radius: 0.3125em;box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"
    src="/img/image_2023-02-07-13-07-25.png"><br>
  <div style="color:orange; border-bottom: 1px solid #d9d9d9;display: inline-block;color: #999;padding: 2px;">Title</div>
</center>

* Cite: Cao Z, Simon T, Wei S E, et al. Realtime multi-person 2d pose estimation using part affinity fields[C]//Proceedings of the IEEE conference on computer vision and pattern recognition. 2017: 7291-7299.
* Available Online: https://arxiv.org/pdf/1812.08008.pdf
* Official Implementation: https://github.com/CMU-Perceptual-Computing-Lab/openpose
* Demo based on OpenCV Implementation: https://github.com/ChrisVicky/OpenCV-OpenPose-Demo
* Date: 2023-02-07

## Brief summary
<center>
  <img style="border-radius: 0.3125em;box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"
    src="/img/image_2023-02-07-12-56-13.png"><br>
  <div style="color:orange; border-bottom: 1px solid #d9d9d9;display: inline-block;color: #999;padding: 2px;">Main Architecture</div>
</center>

* What is the problem the paper is trying to solve?
  - The Speed-up of Multi-Person Pose Estimation Process, the foundation of many behavior-recognizers.

* What are the key ideas of the paper? Key insights?
  - Process all people at once.
  - Part Affinity Fields (PAF).
<center>
  <img style="border-radius: 0.3125em;box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"
    src="/img/image_2023-02-07-12-33-02.png"><br>
  <img style="border-radius: 0.3125em;box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"
    src="/img/image_2023-02-07-12-34-55.png"><br>
  <div style="color:orange; border-bottom: 1px solid #d9d9d9;display: inline-block;color: #999;padding: 2px;">PAF Definition</div>
</center>

* What is the key contribution to the literature at the time it was written?
  - The fastest and most accurate model that recognizes pose information is proposed and implemented by the authors.
  - A New Method that utilizing PAF is presented.

* What are the most important things you take out from it?
  - The idea that using PAF to pair up feature points that belong to one person.
  - The Bottom-Top methodology could reduce redundancy produced by single person recognition in Top-Bottom Methods.

## Strengths (Most Important Ones)

* Does the paper solve the problem well?
  - I suppose yes. The paper presents a higher accuracy compared to other models at that time. And According to my own implementation, the paper wins as well.

## Weaknesses (Most Important Ones)

* Room for improvement.
  - The pair-up process currently is implemented according to an algorithm after the neural network which, in my opinion, could be merged in the network structure.

## How can we do better? Your ideas and thoughts.
* The method relies on a VGG Model that recognizes feature points which can be separated from the main part. Therefore, during video processing where there is a sequence of image data, a pipeline processing structure could be introduced to further improve the efficiency.
* Also, since *VIT*, we may replace the Convolutional Neural Network with **Transformer**.

## What have you learnt/enjoyed/disliked in the paper? Why?
* The bottom-up methodology is the most enjoyed idea. However, the feature extractor on the top still presents a Top-Bottom methodology that, in one hand, does reduce the difficulty of development, but on the other hand betrays the Bottom-Top methodology since the model is topped by a feature extractor.
