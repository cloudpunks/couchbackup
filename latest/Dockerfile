FROM ghcr.io/cloudpunks/alpine:3.19@sha256:c52309fc12c2c1fe77a617f596399d68eef0c1772a75df80f06b169155dc345f
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
