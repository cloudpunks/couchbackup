FROM ghcr.io/cloudpunks/alpine:3.19@sha256:69ad8cd708ea2323fdc112b732de748e7e7281a6a162f0f23c8de99c37e22f1c
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
