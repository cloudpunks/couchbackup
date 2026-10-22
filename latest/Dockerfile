FROM ghcr.io/cloudpunks/alpine:3.24@sha256:6c38f325099639d323a06b213d58fb8b13a9d84b8ef33a7008dba10bbef86246
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.19

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
