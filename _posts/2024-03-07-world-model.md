---
layout: post
title:  "World model from video games"
date:   2015-12-09 00:20:46
categories: jekyll update
published: true
hidden: false
---

Recent developments of AI has highlighted many achievements but the foremost important direction must be mentioned is first constructions of World Model. For the first time in the history of computer science, since the computational viewpoint of anatomy of minds and how it might work was presented in the "Society of Minds" by Marvin Minsky, we have a concrete idea of how the world model could be built. 

But before coming to that point, the philosophical question that mandates our understanding of world models: Are we living in a simulation? The idea of our physical world in fact a perfect simulation run by cosmic-scale and quantum-level computers have been around for many years. People detect resemblances between greatly simple computer games and the world we live in. Only that the sheer scale of complexity paralyzes us from thinking of any possible way to test the hypothesis, not mentioning the ability to understand or build it. 

Not that obscuring anymore. Simulation of the world, or the simulation of our perception about the world, is going to be built from videos. This media format is the most comprehensive form of data in which audio channels are included, and visual perception and action are stored as color pixels in every video frame. This is the best shot from what we have to first mimic the world with some common-sense encoded in it. 

In early 2024 there are two papers have presented their pursuits of such world models. And the commercial video generator called [Sora](https://openai.com/sora) from Open AI. While the latter is truly impressive it is a closed source commercial piece of software that sheds no light into our understanding of progressing the world model prize. 

The first paper comes from Deepmind, 

> Genie: Generative Interactive Environments [arxiv](https://arxiv.org/html/2402.15391v1)

where the authors aim to build a controllable simulation learned from hundreds of hours of platform 2D games. While their results are modest, frames are generated with mediocre visual quality, and controls are limited to a handful of movement actions of 2d sprites such as left, right, jump, it is a proof of concept for a simple world model could be unsupervisedly built from video data. 

The second paper is from Meta research,

> V-JEPA: The next step toward Yann LeCun’s vision of advanced machine intelligence (AMI) [paper](https://scontent-man2-1.xx.fbcdn.net/v/t39.2365-6/427986745_768441298640104_1604906292521363076_n.pdf)

In simple terms this work train a JEPA model, unsupervisedly, on video data. Different from Genie and Sora, V-JEPA does not generate "the world" at pixel space, but learn a latent representation at lower dimensional space. The idea that the visual world could be represented as low dimensional manifolds is old, but it was unclear to design a machine learning model being able to learn anything useful out of sheer amounts of video data. 

Joint Embedding Predictive Architectures (JEPA) is a broad term including architectures that optimize at the same time the encoder of input sensory into low-dim vectorial forms and the predictor that drives plausible transformation of the present input with respect to the arrow of time, a.k.a future states. In this sense, learning from video data makes a lot of sense where frame-to-frame difference encodes state changes over time. 

Genie and V-JEPA share the basic recipe of cooking up a world model. It consists of three parts: i) a *video tokenizer* or *x-encoder* that converts video frames into token / latent embedding *z*, ii) a *latent action model* or *predictor* that infers future states of *z* or actions *a* over *z*, and iii) a *dynamic model* predicts the next video frame given *z* and *a*. The third component however is missing from V-JEPA for good: the authors argue for the succint of embedding whereas the pixel space is extraneous. V-JPEA in its experiments demonstrated the optional third component by training a pixel decoder which gives no nonsense pixel-level reconstruction of predicted states *z*. 

At the abstract level there is virtually no differences between Genie and V-JEPA except that Genie made use of a discrete model called Vector Quantized Variational Autoencoder (VQ-VAE) to compress the continuous latent control predictive space to a few codebooks which correspond to sprite movements such as up, down, left, right. The most important message from the papers nevertheless is that video data is the key to train the next AI models without relying on expensive annotations. As a result, scaling compute is the only best way to improve  the quality of these video-based world model. A trillions parameters model trained on all of the GPUs in the world from all the videos available on YouTube will give you something blow up your mind.

