## 用途

- コードのビルド、テスト、デプロイなどのプロセスを自動化
- リリースノートやリリースのソースなどを自動作成
- Java や Python などの環境を自動的に構築
- プルリクエストしたことなどを、Slack やメールなどで自動通知
- プッシュの都度、JavaScript の Lint を実行
- コードスタイルのチェック
- セキュリティスキャンの実行

## 使えそうなやつ

- テスト用のイメージbuild
- リリースノート作成
  - documentにも転用できていいかも
- formatter, phpcs-fixer の自動PRを出してくれる
- reviewdog
  - テスト結果をprにコメントしてくれる
- gptなどがPRレビューをしてくれる
  - PR-Agent というライブラリがある
    - openAIのラッパーみたいな雰囲気
  - これを bedrock などを参照させるようにすればいいか
  - configration file のmodelを変更するだけで基盤モデルを変えられるらしい
    - https://github.com/Codium-ai/pr-agent/blob/2102c514225159aa5e53d6de477a6ea3c942e300/docs/docs/usage-guide/changing_a_model.md#changing-a-model
  ```
    [config]
    model = "..."
    model_turbo = "..."
    fallback_models = ["..."]
  ```

## 参考

- [GitHub Actionsでいい感じのリリースノートを完全自動で作成する](https://zenn.dev/kshida/articles/auto-generate-release-note-with-calver#%E5%89%8D%E5%9B%9E%E3%81%8B%E3%82%89%E3%81%AE%E5%B7%AE%E5%88%86%E3%82%92%E3%82%82%E3%81%A8%E3%81%AB%E3%83%AA%E3%83%AA%E3%83%BC%E3%82%B9%E3%83%8E%E3%83%BC%E3%83%88%E3%81%AE%E6%9C%AC%E6%96%87%E3%82%92%E7%94%9F%E6%88%90%E3%81%99%E3%82%8B)
- [メルコインにおけるGitHub Actions活用術](https://engineering.mercari.com/blog/entry/20231223-mercoin-github-actions/)
- [コードとブログの両方を効率的にレビューする仕組みについて：PR-Agent（Amazon Bedrock Claude3）の導入](https://blog.kinto-technologies.com/posts/2024-06-17-pr-agent/)
