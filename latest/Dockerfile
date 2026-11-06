FROM ghcr.io/cloudpunks/alpine:3.24@sha256:1aa42e6acf3d3ba10b3edd39469425e03cc3edcc4e25b387ac466ccbd08fa727
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.20

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
