# build container image
## build
```bash
docker build -t <image name>:<tag> .
```

e.g)
```bash
docker build -t my-project/my-app:1.0 .
```

## run
```bash
docker run --rm -it -p 8000:8000 -v ${PWD}:/workdir my-project/my-app:1.0
```

* --rm: exit と同時にコンテナを削除する
* -p: コンテナへアクセスするポートを指定
* -v: ホストOS のディスクをつける。ホスト側:コンテナ側 

