# 理解した範囲での概要
APIのクエリ言語、らしい。  
クライアントサイドとサーバーサイド間の通信の規格、というか方法のことだという理解

# クライアントサイドから見た使い方
おそらくだいたいgraphql用のエンドポイントが用意されているので、そのエンドポイントに対してクエリリクエストを投げる

## 例
GithubがGraphQL用エンドポイントのプロキシを用意してくれており、それがわかりやすい
<https://developer.github.com/v4/explorer/>

エンドポイント: `https://graphql-explorer.githubapp.com/graphql/proxy`
リクエストのペイロード: 

```graphql
{
  viewer {
    login
  }
}

```

レスポンス:

```json
{
  "data": {
    "viewer": {
      "login": "Githubアカウント名"
    }
  }
}
```

# その他
GraphQL自体は通信プロトコルの規定などがないので、HTTP以外もあるっぽい。RPCとか。
https://qiita.com/bananaumai/items/3eb77a67102f53e8a1ad#fnref1

# わからないこと
- RESTfulとかと同じレイヤーの概念って理解で合ってる？
- Githubのプロキシ、試してみると全部POSTでリクエストが送られているのだが、GraphQLの作法ってそういうものなのだろうか？

# 参考文献
[Introduction to GraphQL](https://graphql.org/learn/)  
[GraphQL入門 - 使いたくなるGraphQL](https://qiita.com/bananaumai/items/3eb77a67102f53e8a1ad)