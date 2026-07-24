FROM ghcr.io/cloudpunks/alpine:3.19@sha256:26a7a6ce1571f7f57ecefab00f734eb3a6ebc0baa42d55b208244a3e01868a13
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
