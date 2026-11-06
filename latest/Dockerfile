FROM ghcr.io/cloudpunks/alpine:3.24@sha256:9482e5bfa69beff273ddfc00004f101cb03760c7d98d0a727377fc30f7aff66a
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.20

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
