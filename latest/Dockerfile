FROM ghcr.io/cloudpunks/alpine:3.24@sha256:1ff90666d642910c31f8643e00b9fae907e95f500a82a2e1c2becc96b6e9c3e9
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.19

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
