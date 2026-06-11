FROM ghcr.io/cloudpunks/alpine:3.19@sha256:ea97c664286d853d4465b1a37ed948a35c536c7e9d854f8114847673272d08bd
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
