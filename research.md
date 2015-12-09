---
layout: page
title: Research
permalink: /research/
---
### Deep Representation Learning and Noisy Data ###
![Deep](assets/thumbnails/deep.png)
The keep-growing content of Web images may be the next important data source to scale up deep neural networks, which recently obtained a great success in the ImageNet classification challenge and related tasks. This prospect, however, has not been validated on convolutional networks (convnet) – one of best performing deep models – because of their supervised regime. While unsupervised alternatives are not so good as convnet in generalizing the learned model to new domains, we use convnet to leverage semi-supervised representation learning. Our approach is to use massive amounts of unlabeled and noisy Web images to train convnets as general feature detectors despite challenges coming from data such as high level of mislabeled data, outliers, and data biases.

>**References**
>
>1. Phong D. Vo, Alexandru Ginsca, Herv\'e Le Borgne, Adrian Popescu, **On Deep Representation Learning from Noisy Web Images**, arXiv, 2015.
>2. Phong D. Vo, Alexandru Ginsca, Herv\'e Le Borgne, Adrian Popescu, **Effective Training of Convolutional Networks using Noisy Web Images**, CBMI, 2015.

### Transductive Kernel Learning ###
![Semantic Visualization](assets/thumbnails/tkl.png)
Transductive inference techniques are nowadays becoming standard in machine learning, but their success remains highly dependent on the choice of kernels, which are usually handcrafted or designed in order to capture better similarity in training data. We introduce a novel transductive learning algorithm for kernel design and classification. Our approach is based on the minimization of an energy function mixing i) a reconstruction term that factorizes a matrix of input data as a product of a learned dictionary and a learned kernel map ii) a fidelity term that ensures consistent label predictions with those provided in a ground-truth and iii) a smoothness term which guarantees similar labels for neighboring data and allows us to iteratively diffuse kernel maps and labels from labeled to unlabeled data. Solving this minimization problem makes it possible to learn both a decision criterion and a kernel map that guarantee linear separability in a high dimensional space and good generalization performance.

>**References**
>
>1. Phong D. Vo, **Transductive Inference for Image Interpretation and Search**, Doctoral disseration, TELECOM ParisTech, 2014 (Chap. 3)

### Semantic Visualization ###
![Semantic Visualization](assets/thumbnails/satellite.png)
We extend our transductive kernel learning approach to subspace problem which enables potential applications such as dimensionality reduction, ranking, and search. Instead of learning a kernel map for classification purpose, we learn a low dimensional embedding resided in the subspace defined by given semantic concepts with few training examples. This new representation is expected to preserve global topology while expose semantic dynamics of the data, which is expected to be useful for data visualization.

>**References**
>
>1. Phong D. Vo, Hichem Sahbi, **Semantic Subspace Learning for Mental Search in Satellite Images**, IGARSS, 2013.
>2. Phong D. Vo, Hichem Sahbi, **Spacious: An Interactive Mental Search Interface**, ACM SIGIR, 2013. 
>3. Phong D. Vo, **Transductive Inference for Image Interpretation and Search**, Doctoral disseration, TELECOM ParisTech, 2014 (Chap. 6)

### Scene Understanding ###
![Semantic Visualization](assets/thumbnails/parse.png)
Scene parsing is a machine vision task that comprises localizing all available objects in an image and then classifying them into known categories. As scene image is a capture of landscape in the real world, the number of objects can vary from few to hundreds. Their categories can be any of among existing man-made structures, plants, human, and animals. In the one hand, such rich set of visual taxonomy limits vision algorithm’s scalability. In the other hand, the intra-variance within every category makes those algorithms generalize hardly to unseen or rare object appearances. We address a new scene parsing algorithm which based on algorithm transductive kernel learning.

>**References**
>
>1. Phong D. Vo, **Transductive Inference for Image Interpretation and Search**, Doctoral disseration, TELECOM ParisTech, 2014 (Chap. 5)

### Automatic Image Annotation ###
![Semantic Visualization](assets/thumbnails/annot.png)
With the exponential growth of multimedia sharing spaces, such as social networks, visual contents are nowadays abundant. Searching these large collections requires a preliminary step of image annotation that translates visual contents into labels also known as keywords or concepts. Automatic image annotation is challenging due to the perplexity when assigning many possible labels to images and the difficulty to analyze rich and highly semantic contents. In annotation, image observations are first described using low-level features (color, texture, shape, etc.), and labels are then assigned to images. The goal is to model the correspondence between low level features and labels in order to predict keywords for unlabeled images. In this context, our learning algorithm (transductive kernel learning) is extended into a multi-labels classification problem.

>**References**
>
>1. Phong D. Vo, Hichem Sahbi, **Modeling Label Dependencies in Kernel Learning for Image Annotation**,  ICIP, 2014.
>2. Phong D. Vo, Hichem Sahbi, **Transductive Kernel Map Learning and Its Application to Image Annotation**, BMVC, 2012

### Interactive Images Segmentation ###
![Semantic Visualization](assets/thumbnails/segm.png)
We use the Pascal VOC 2011 dataset in order to evaluate the performance of on object class segmentation (OCS). We use 556 images belonging to 21 categories; given an image, the goal is to assign each group of pixels (referred to as superpixel) to one of these 21 categories. A given image is subdivided into an irregular grid of 700 superpixels, each one is processed in order to extract various features. For each image in VOC, we turn OCS into a transductive inference problem where only a small fraction of its underlying superpixels is labeled. We train one transductive classiﬁer for each category and we combine these classiﬁers using the “winner-take-all” strategy in order to infer the category of a given unlabeled superpixel.

>**References**
>
>1. Phong D. Vo, Hichem Sahbi, **Transductive Inference & Kernel Design for Object Class Segmentation**, ICIP, 2012
