# Static site Generator
## Material for MkDocs
mkdocs にMaterial を加えたコンテナイメージ
* [squidfunk/mkdocs-material on dockerhub](https://hub.docker.com/r/squidfunk/mkdocs-material/)
* [squidfunk/mkdocs-material on GitHub](https://github.com/squidfunk/mkdocs-material)

### How to use
* Start development server on
```
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
```

Webブラウザにて127.0.0.1:8000 へアクセスすると、変換されたページを参照できる。


* Build documentation
```
docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build
```

ビルドが完了するとsite フォルダに変換されたファイル群が生成される。
