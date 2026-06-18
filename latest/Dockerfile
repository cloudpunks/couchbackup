FROM ghcr.io/cloudpunks/alpine:3.19@sha256:4d9e4caea8b63ce9d1648e33e2a861ad74c9f357d44a67f712344a320300de85
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
