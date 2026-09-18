FROM ghcr.io/cloudpunks/alpine:3.24@sha256:f735e3f0ae5b8ab423c6467079a33c38e2700eab720cc676f5a330b44eb9d05d
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.19

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
