FROM ghcr.io/cloudpunks/alpine:3.19@sha256:cc94b01dc81fa3c23a8a4e203a24ba7017b0230c6de68e77a025fe11a5848888
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
