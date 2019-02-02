---
title: Hawkes process papers notes
author: BY
layout: post
---
## Classic Paper
First proposed by Alan Hawkes as [self-exciting point process](https://academic.oup.com/biomet/article/58/1/83/224809). [Hawkes and Oakes](https://www.cambridge.org/core/journals/journal-of-applied-probability/article/cluster-process-representation-of-a-selfexciting-process/E836A3D07D808068E2F9F3E7E366B081) further developed a Poisson clustering process representation - very useful for [simulation](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2003JB002879), [declustering](https://www.jstor.org/stable/3085650?seq=1#metadata_info_tab_contents) and order bounds. 

Later Yosihiko Ogata used Hawkes process to model earthquake after-shocks events in his seminal papers on [temporal](https://www.tandfonline.com/doi/abs/10.1080/01621459.1988.10478560) and [spatiotemporal](https://link.springer.com/article/10.1023/A:1003403601725) cases. They also provide evaluation methods such as transformed time. For spatiotemporal, [Voronoi cells](https://projecteuclid.org/euclid.aoas/1419001742) are used to address the uneven distribution in space.  

The estimation of Hawkes process is an interesting direction with many open problems. EM-Type algorithm proposed by [Veen and Schoenberg](https://www.tandfonline.com/doi/abs/10.1198/016214508000000148) is related to the nonparametric method by [Marsan and Lengline](http://science.sciencemag.org/content/319/5866/1076). Many papers are looking for faster algorithms in the multivariate case because the number of parameters and data, such as a recent [cumulants-based method](http://jmlr.org/papers/volume18/17-284/17-284.pdf). There is a good [review paper](https://projecteuclid.org/euclid.ss/1534147221) by Alex Reinhard for Spatiotemporal Point processes.

## Applications
### Crime
George Mohler's [JASA paper](https://amstat.tandfonline.com/doi/abs/10.1198/jasa.2011.ap09546) uses nonparametric Hawkes process to model crimes in LA and [another paper](https://www.sciencedirect.com/science/article/pii/S0169207014000284) uses a KDE background method for Chicago crimes..... I am recently working on a gang violence intervention program in LA using multivariate Hawkes processes and also find this model is useful for retailation behaviors.


### Network
Multivariate Hawkes processes (connection to [Granger causality](https://onlinelibrary.wiley.com/doi/full/10.1111/jtsa.12213)) are used to reconstruct networks. Examples: [Email network](https://www.tandfonline.com/doi/abs/10.1080/01621459.2015.1135802) using temporal Hawkes with background rate periodic in time (other choices of inhomogeneous background rate in time: [KDE](http://paleo.sscnet.ucla.edu/Lewis-Molher-EM_Preprint.pdf) and [log Gaussian Cox process](https://projecteuclid.org/euclid.aoas/1380804805)); [Bayesian Hawkes](http://proceedings.mlr.press/v32/linderman14.pdf) uses a temporal Hawkes with random graph prior; [Beyond Mutual Excitation](https://arxiv.org/pdf/1707.04928.pdf) considers inhibitions; We have a [recent paper](https://arxiv.org/abs/1811.06321) considering spatiotemporal case. 
Interesting connection to dynamic [graph embeddings](https://ieeexplore.ieee.org/document/8294302/).

### Epidemic
#### Socal media
Many papers(see [a review](https://arxiv.org/pdf/1708.06401.pdf)) are using Hawkes process to model contagious on social media such as retweeting. I got some interesting results when using Hawkes process to model tweet topics from NMF in a [REU project](https://academic.oup.com/imamat/article/81/3/409/2871030). Currently working on other applications of Hawkes topic model.
#### Disease
Connection to SIR.