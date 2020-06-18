# MkDocs
## DockerFile
コンテナを自作する場合のDockerFile の走り書きメモ。これに好みのライブラリを追加、バージョン指定をして

```Dockerfile
FROM python:3.8.1-alpine3.11

RUN pip install --upgrade pip \
  && pip install mkdocs \
  && pip install mkdocs-material

# Set working directory
WORKDIR /docs

# Expose MkDocs development server port
EXPOSE 8000

# Start development server by default
ENTRYPOINT ["mkdocs"]
CMD ["serve", "--dev-addr=0.0.0.0:8000"]
```

## 参考
### Dockerfile
* [squidfunk/mkdocs-material のDcokerfile](https://github.com/squidfunk/mkdocs-material/blob/master/Dockerfile)
* [【年末大掃除】.mdをCI/CDで整理する at OPTim TECH BLOG](https://tech-blog.optim.co.jp/entry/2019/12/25/173000#dockerfile)
