# painters_by_numbers
Deep Learning Project

In this project we have evaluated approaches to the challenge proposed on Kaggle named {Painter by Numbers}. The objective of this challenge is to distinguish whether two paintings were created by the same artist in the process of pairwise comparison. In a broad sense this could improve the identification of forgeries based on learned {artist style}. The dataset for the challenge is a collection of paintings from WikiArt.org {http://wikiart.org}. After analyzing approaches taken by other competitors, we have identified a gap that could be explored: creating a network that not only learns the style from artists included in the provided dataset, but also is able to give a correct verdict for an artist that are not included in the training data. This creates an additional layer of complexity as the network has to facilitate ability to {generalize to unseen artists}. To tackle the problem at hand, a neural network architecture called the siamese network was used.

After the analysis of approaches submitted by other competition participants, a baseline architecture was chosen. Another approach that was explored is a siamese network composed of two symmetric branches, using equal weights of a pretrained Xception state-of-the-art CNN. In the following sections these architectures are explored  and analyzed in the context of generalization performance on unseen data. Further improvements are proposed with regards to data set augmentation and architecture modification. Altogether, three hypotheses are to be evaluated:

* {Hypothesis 1}: As a baseline model, how well can the CNN-based siamese network trained on the paintings dataset perform well in terms of generalisation error?
    
* {Hypothesis 2}: Will a siamese network trained on pre-trained features outperform the baseline CNN model? 
    
* {Hypothesis 3}: Can further fine-tuning of the pre-trained features and feature representations give a better generalisation for unseen artist?

