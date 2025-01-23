---
title: "PMGNN: A Pioneer-Master Graph Neural Network for Graph Classification"
collection: publications
date: 2022-07-18
excerpt: 'This paper proposes a.'
venue: 'IJCNN'
paperurl: 'https://ieeexplore.ieee.org/document/9892849'
citation: 'Tan, Ruifeng, and Yuanyuan Zhu. "PMGNN: A Pioneer-Master Graph Neural Network for Graph Classification." 2022 International Joint Conference on Neural Networks (IJCNN). IEEE, 2022.'
---


**Abstract:** Graph classification task has attracted increasing interest in recent years due to its application in a wide range of domains, and graph neural networks (GNNs), especially the attention-based ones, are proved to be highly effective in this task. However, existing attention-based GNNs have a limited receptive field since the attention weights are computed only based on the information obtained from the direct neighbor nodes. Moreover, they cannot flexibly adjust vectors for attention weight computation considering both current and history node embeddings. In this paper, we propose a novel graph neural network named Pioneer-Master Graph Neural Network (PMGNN) to achieve a better attention mechanism, which is composed of two modules. The first is a pioneer network, which utilizes a GNN to collect context information from multi-hop neighborhoods to increase the receptive field and keep the history node embeddings. The second module is a master network, which exploits the hierarchical attention module to generate the global view from the context information, and combines the global view with the instant view to achieve a better attention mechanism. Extensive experimental results on four real-world datasets demonstrate the effectiveness of our model compared with a series of state-of-the-art baselines.




