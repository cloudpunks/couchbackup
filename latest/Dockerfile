FROM ghcr.io/cloudpunks/alpine:3.24@sha256:dac428a9b6d3aa41809f34a428ee8550a4f2ba99d82c75e9689d4cf055fc2e78
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.19

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
