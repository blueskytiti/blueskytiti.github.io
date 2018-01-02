## MISC

**The efficient estimation of word representations in vector space, 2013, mikolov**
- summary: goal is learn high quality words vectors from very large datasets, 
-  aim to preserve vector operations (offsets) eg vector(”King”) - vector(”Man”) + vector(”Woman”) = vector that is closest to the vector(Queen) 
- techniques based on contious bag of word model (predicts current word based on context)
- continous skip-gram

## GANS

**about GANS in general:**
- technique that learns 2 networks (a generator and a discriminator) with competing losses. The aim of the generator network is to map a random vector to a realistic image, the aim of the discriminator is to distinguish the generated from the real images
- maps a random vector into an image that is supposed to be realistic
training uses s a two-player minimax game: update the image synthesis network, and the discriminator network, alternatively

***Improved techniques for training GANs, Salimans et al, 2016**
- link: <http://papers.nips.cc/paper/6125-improved-techniques-for-training-gans.pdf>
- summary: 
- approach:  
- other

***Generative adversarial nets, Goodfellow et al, 2014**
- link: <http://papers.nips.cc/paper/5423-generative-adversarial-nets.pdf>
- summary:  original paper on GANs
- approach:  compete a generative model that generates and image and a discriminative model that detects what is 'fake', both joined at the hip via a loss function, and a training procedure using minimax two player game

***Learning from Simulated and Unsupervised Images through Adversarial Training, Shrivastava et al, Apple, 2017**
- link: <https://arxiv.org/abs/1612.07828>
- summary: a hybrid physics simulation and GAN like approach to novel image generation
- approach:  mod to GAN loss function including: (i) a 'self-regularization' term, (ii) a local adversarial loss, (iii) updating the discriminator using a history of refined images. 
- other: 
- learn a model that improves the realism of synthetic images from a simulator using unlabeled real data
by using the annotation information from the simulated data
- takes simulated + label data through a net that improves 'realism' (called refiner net), and do adversarial training on it (via a real vs simulated discriminative net).
- traditional GAN: learns 2 networks (a generator and a discriminator) with competing losses. The aim of the generator network is to map a random vector to a realistic image, the aim of the discriminator is to distinguish the generated from the real images.
Q: what is the second term in equation (1), is it wrt to 
the task of classifying the image (gaze) or wrt to telling if it's real or sythetic?


## Un/semi-supervised, X-shot (zero, one, adaptive), generative

***Building high-level features using large scale unsupervised learning, Le et al, 2012**
- link: <http://arxiv.org/pdf/1112.6209>
- summary: build feature detectors from unlabeled data
- approach:  hows that can build face detector without using any labeled faces
- other:
	

***pixel recurent neural networks, van der ord et al, google, 2016**
- link <http://arxiv.org/pdf/1601.06759v2.pdf>
- summary:  with goals to synthesize images and reminiscent of MRF uses recurrent nets (eg LSTMs) to predict each pixels in a causal fashion
- approach:  
- other: 

***Deep Photo Style Transfer, Luan et al, 2017**
- link: <http://arxiv.org/pdf/1703.07511v1.pdf>
- summary: style transfer via CNN
- approach: constrains transformation from input to output to  locally affine in colorspace, express this constraint as a custom CNN layer through which they can backpropagate
- other:

**Unsupervised representation learning with deep convolutional generative adversarial networks, A. Radford et al, 2015**
- link <https://arxiv.org/pdf/1511.06434v2>
- summary: some improvements on GANs architecture
- approach:  uses all convolutional network; batch normalization; uses visualization. 
- other: 

**Auto-encoding variational Bayes, Kingma et al, 2013**
- link <http://arxiv.org/pdf/1312.6114>
- summary: 
- approach:  
- other: 
- Q: 

**Zero-Shot Learning Through Cross-Modal Transfer, 2013**

- link <https://arxiv.org/pdf/1301.3666.pdf>
- summary: using outlier detection in the semantic space to improve performance of seen+unseen class classifier
- approach: embedding in joint image-text space
- summary: 
- approach:  
- other: 
- Q: 

***DRAW: A recurrent neural network for image generation, Gregor et al, 2015**
- link <http://arxiv.org/pdf/1502.04623>
- code <https://github.com/ericjang/draw>
- summary: a image synthesis approach based on autoencoder framework using attention mechanism
- approach:  
- other: 
- Q: 

**isolation forest, liu, 2008**

- link <https://cs.nju.edu.cn/zhouzh/zhouzh.files/publication/icdm08b.pdf>
- build a tree, e.g. a CART based on some features, it should be the case the anomaly stand on their own at the top (because there are few of them and they are distinct)
- use of forest of these

## DRL

**Leveraging deep reinforcement learning for reaching robotic tasks, Katyal et al., 2017**

- citation [@katyal2017leveraging]
- summary: control policy that is robust to changes and does not need calibration. Applied to reaching robotic tasks.
- approach: uses DRL and DQL 

**Collaborative Deep Reinforcement Learning for Joint Object Search, Kong et al, 2017**

- citation: [@kong2017collaborative]
- summary: active search of interactive object, eg. situations where different objects often appear with certain correlated patterns, e.g. person riding bicycle, cups on table
- approach: collaborative multi-agent DRL, multi-agent Q-learning, 


**Active object localization with deep reinforcement learning., Caicedo et al, 2015**

- cite: [@caicedo2015active]
- summary: DRL applied to active search of object
- approach: BB modified according to discrete action space, size 9, {move right, move left, move up, move down, scale bigger, scale smaller, aspect ratio change fatter, aspect ratio change taller, trigger}
- deep Q-learning
- reward is based IOU

**Mitigation of Effects of Occlusion on Object Recognition with Deep Neural Networks through Low-Level Image Completion, Chandler et al, 2016**

- cite: [@chandler2016mitigation]
- [link to paper](https://www.hindawi.com/journals/cin/2016/6425257/)
- summary:  object recognition via DCNN is affected by occlusion 
- approach: provides new dataset that emphasizes occlusion and methods to address this, including preprocessing by segmenting occlusion and inpainting.

## Adverserial

***Deep neural networks are easily fooled: High confidence predictions for unrecognizable images ,  Nguyen et al, 2015**
- 


## Classification, detection, localization


## Face

**REGULARIZING FACE VERIFICATION NETS FOR PAIN INTENSITY REGRESSION, Hager, 2017**
- https://arxiv.org/pdf/1702.06925.pdf
- summary:
- method:

**Neural Face Editing with Intrinsic Image Disentangling, cvpr2017, samaras**

- summary: 
- uses GANs to desentagle latent representation of face so that can keep surface normals fixed while changing some semantic properties like facial expression (smiling) or presence of glasses or age
- learns useful manifold of facial appearance
- relevant for: autism , discovery, ML
- approach:
- have (approximate) models for facial appearance in terms of intrinsic face prop- erties like geometry (surface normals), material properties (diffuse albedo), and illumination. 
- leverage this by de- signing the network to explicitly infer these properties and introducing an in-network forward rendering model that re- constructs the image from them. 
- uses priors on these properties
- ensures fidelity by adversarial supervision
- uses mating to separate fore from background
- "We show that by constraining physical properties that do not affect the target edits, we can achieve significantly more realistic results compared to other learning-based face editing approaches."
- net is physicallly grounded by ex- plicit in-network representations of its shape, albedo, and lighting.
- relevant for: autism , discovery, ML, synthetic reconstruction of rare data 

**Fast Video Classification via Adaptive Cascading of Deep Models, cvpr 2017, krishamurphy **
- summary: 
- approach:
- online bandit problem
	- structure the classifier as a cascade (or tree [30]) of simple classifiers such that “easy” examples lead to early exits and are therefore classified faster.
- relevant for:
- code: 
