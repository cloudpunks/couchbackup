FROM ghcr.io/cloudpunks/alpine:3.19@sha256:20ab65b98d0b0339b27c44756472b1984be81f7f5a904a9fb36d6cf960e8c5cc
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
