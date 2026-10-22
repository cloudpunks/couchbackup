FROM ghcr.io/cloudpunks/alpine:3.24@sha256:91e446169b936cbc2d4a9a269181f583f466518dc6a80c6baaa3d28a212a5660
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.19

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
