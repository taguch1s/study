## Abst
[Graph Learning for Exploratory Query Suggestions in an Instant Search System](https://research.atspotify.com/2023/10/graph-learning-for-exploratory-query-suggestions-in-an-instant-search-system/)

- グラフ構造ベースで関連クエリをサジェスト
- 複数の属性でも近いものを提示できるというのが良さそう
  - node2vecを使用しているらしいが、node2vecに複数の属性を表現する方法あったか??
    - node2vec自体は同次グラフ(単一のノードタイプとエッジタイプを持つグラフ)対称
      - https://deus-ex-machina-ism.com/?p=56947
    - 詳細不明ではあるが、HeteroGenerous Graph + Random Walk でnode2vec的な手法ですよ、的な話かも
- 検索クエリからグラフ近傍検索を行うためのEmbeddingとかなにか行っている？
  - Graph構造のみだと、一致した単語からの近傍しか辿れない
  - これはこれでそういうものなのかも
  - サジェストの結果が0件だったらembedding変換投げるとかでもいいかも
