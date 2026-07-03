FROM ghcr.io/cloudpunks/alpine:3.19@sha256:0b956a6f42aa44573489a3057d09b86b6adbd404421b4119902b042345339299
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
