---
layout: post
title: A Summary of Transformer-based Architectures in Computer Vision
date: 2015-03-15 16:40:16
description: we review modern vision architectures related to transformer.
tags: ViT CV ImageNet
categories: computer visionn
---

In this article, we review modern vision models that are related to Transformer architecture. Spanning from vanilla ViT toward MetaFormer, we describe each architecture in detail with visual schematics and formulas.

## ViT 
[An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://arxiv.org/abs/2010.11929)

ViT successfully adapts transformer architecture in computer vision for the first time, outperforming other CNN-based architectures with fewer computational resources, while it is more specialized to classification tasks. The authors claim that to make such an architecture work, a pretraining on large amounts of data was necessary since transformer provides no inductive bias such as translation invariance in CNN, which might have eased the training on small datasets.

ViT simply divides an image into multiple fixed-size patches (i.e. 16x16 in this paper) and treat those as same as word embeddings in NLP. Concretely, each patch is transformed into a vector by a linear layer and is processed by the Transformer encoder as follows.