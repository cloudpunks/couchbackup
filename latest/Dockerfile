FROM ghcr.io/cloudpunks/alpine:3.19@sha256:b6326bdeb79bd21dfe730daaa67c16598acf9f345590781bcaad5b12459f07ac
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
