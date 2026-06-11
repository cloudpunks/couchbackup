FROM ghcr.io/cloudpunks/alpine:3.19@sha256:f0d0e20158b4757ab2476ae46aa1df529253ad49d9a22446e5dc222aaf1870f8
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
