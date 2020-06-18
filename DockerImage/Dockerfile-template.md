# template for python
## Dockerfile
```Dockerfile
# base image https://hub.docker.com/_/python
FROM python:3.8.1-alpine3.11

# install libs
WORKDIR /tmp
COPY ./requirements.txt requirements.txt

RUN pip install --upgrade pip \
  pip install -r requirements.txt

# Set working directory
WORKDIR /docs

# Expose server port
EXPOSE 8000

# Set commands
ENTRYPOINT ["hoge"]
CMD ["serve", "--dev-addr=0.0.0.0:8000]
```

## requirements.txt
example
```
hoge==1.0
fuga==1.0
...
```
