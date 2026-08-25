FROM ghcr.io/cloudpunks/alpine:3.19@sha256:b7fa9c5a5990efcb67547792780480668730c2a72ded5b2bd123effdcad7174d
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.19

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
