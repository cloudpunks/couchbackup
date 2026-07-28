FROM ghcr.io/cloudpunks/alpine:3.19@sha256:8fc1fa1305afb6acb25274d28e875806c06df5922e8c940a6b85bb1f5d5dc8e6
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
