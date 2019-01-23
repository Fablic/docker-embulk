# docker-embulk

An AlpineLinux Embulk docker container.

## Docker Tags

- [`0.9.13-alpine3.8`, `latest`](https://github.com/fablic/docker-embulk/tree/master/0.9.13/alpine3.8/Dockerfile)

## How to use

For example.

```dockerfile
FROM fablic/embulk:latest

RUN adduser -D embulk
USER embulk

RUN embulk gem install \
        embulk-input-mysql \
        embulk-output-bigquery

WORKDIR /usr/src
COPY --chown=embulk:embulk . .
```
