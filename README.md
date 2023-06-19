<div align="center">

<h2> Graph Contrastive Learning with Constrained Graph Data Augmentation </h2>

Shaowu Xu<sup>1</sup>, Luo Wang<sup>1</sup>, [Xibin Jia](https://scholar.google.com/citations?user=0XxocmcAAAAJ&hl=en&oi=ao)<sup>1</sup>

 
<sup>1</sup>[Beijing University of Technology](https://www.bjut.edu.cn/)

</div>

***

This is the official implementation of our proposed two constraint principles for graph augmentation, LDP (low dissimilarity priority) and mutual exclusion (ME). The backbone model used in the graph classification experiments is [GraphCL](https://github.com/Shen-Lab/GraphCL/tree/master) that takes NT-Xent for graph-structured data as the optimization objective. The backbone model used in the node classification experiments is [GCA](https://github.com/CRIPAC-DIG/GCA), using the improved InfoNCE as the loss function.

## Overview
**Abstract:** Studies on graph contrastive learning, which is an effective way of self-supervision, have achieved excellent experimental performance. 
		Most existing methods generate two augmented views, and then perform feature learning on the two views through maximizing semantic consistency.
		Nevertheless, it is still challenging to generate optimal views to facilitate the graph construction that can reveal the essential association relations among nodes by graph contrastive learning.
		Considering that the extremely high mutual information between views is prone to have a negative effect on model training, a good choice is to add constraints to the graph data augmentation process. 
		This paper proposes two constraint principles, low dissimilarity priority (**LDP**) and mutual exclusion (**ME**), to mitigate the mutual information between views and compress redundant parts of mutual information between views.
		LDP principle aims to reduce the mutual information between views at global scale, and ME principle works to reduce the mutual information at local scale. They are opposite and appropriate in different situations.

![LDP](docs/LDP.svg)
**Fig. 1** The schematic diagram of the proposed LDP principle, taking node dropping as example. The color depth of each node represents its dissimilarity with the anchor nodes, with darker colors indicating lower dissimilarity.

![ME](docs/ME.svg)
**Fig. 2** The schematic diagram of the proposed ME principle, taking node dropping as example. The red and blue nodes represent nodes belonging to different subsets of nodes.
