FROM ghcr.io/cloudpunks/alpine:3.19@sha256:f53d30f105636aff5d02554ded8d8a2b23129224bfe8cbf0fc702649b386f57e
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
