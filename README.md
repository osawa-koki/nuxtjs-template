# simple-nuxt-study.ssg.ts

Nuxt.jsの学習用プロジェクト。  

## 実行方法

```shell
# モジュールのインストール
yarn

# デバグ用実行
yarn dev

# ビルド
yarn generate
```

## 補足

~~Nodeのバージョンが16よりも新しいとデバグ実行時に`digital envelope routines::unsupported`というエラーが発生するるため、DevContainerを使用してNode16を用いて開発を行う。~~  

DevContainer内ではなぜかホットリロードができなく、開発が困難であるため、[nvm](https://github.com/coreybutler/nvm-windows/releases)を使用して一時的にホストNodeのベージョンを下げる。  
不本意ながら。  
