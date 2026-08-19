FROM ghcr.io/cloudpunks/alpine:3.19@sha256:17c393a33034e12ca4ba9a263e8c81358ae8fb3ecfc146f7de2f7ba10ef935b6
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
