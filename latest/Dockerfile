FROM ghcr.io/cloudpunks/alpine:3.19@sha256:381202025a6f09a9525ed978405d93898fb8c490f6dcc7dbd3ce3a0adbcffccf
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
