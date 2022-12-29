# nuxtjs-template

Nuxt.jsで自分がよく使うテンプレート。  

## 補足

Nodeのバージョンが新しすぎることにより暗号化エラー``が発生することがある。  
したがって、以下のコマンドに変更することで一時的に回避している。  

```shell
- nuxt
+ nuxt --openssl-legacy-provider
```
