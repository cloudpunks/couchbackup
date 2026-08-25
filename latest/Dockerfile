FROM ghcr.io/cloudpunks/alpine:3.24@sha256:c05a9a0ce1b3d9e2f216b0024f499a562977cfa67174c20e9f9a19dee301ad04
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.19

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
