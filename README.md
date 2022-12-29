# nuxtjs-template

Nuxt.jsで自分がよく使うテンプレート。  

## 実行方法

```shell
# デバグ実行
yarn dev

# ビルド
yarn generate
```

## 補足

Nodeのバージョンが新しすぎることにより暗号化エラー`digital envelope routines::unsupported`が発生することがある。  
したがって、以下のコマンドに変更することで一時的に回避している。  

```shell
- nuxt
+ nuxt --openssl-legacy-provider
```
