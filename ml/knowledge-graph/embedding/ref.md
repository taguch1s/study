# refs
良さそうなもののまとめ

- [UNDERSTANDING GRAPH EMBEDDING METHODS AND THEIR APPLICATIONS](https://arxiv.org/pdf/2012.08019)
  - Multi-hop based と Random-walk based の近傍サンプリング方法がある
    - いまいち明示されてなくて、ちゃんと認識できてなかった
- [A Comprehensive Survey of Graph Embedding: Problems, Techniques and Applications](https://arxiv.org/pdf/1709.07604)
  - graph embedding techs は大きく分けて以下
    -  Matrix Factorization
       -  Graph Laplacian Eigenmaps
       -  Node Proximity Matrix Factorization
    -  Deep Learning
       -  DL based Graph Embedding with Random Walk
          -  Node2vec, metapath2vec, ...
       -  DL based Graph Embedding without Random Walk
          -  SDNE などの autoencoder
             -  Graph Convolutional Networks, Graph Attention Networks, Graph Neural Networks もencoderなのでここ
          -  transE,transR, Rescal, Complex などもここに入ってくるのだろうか
       -  その他は node embedding とは無関係っぽいので割愛
