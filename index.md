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