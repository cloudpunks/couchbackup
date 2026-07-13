FROM ghcr.io/cloudpunks/alpine:3.19@sha256:25b5279743053a31300d52aeea02743c57b9e613fb67d2a87628383ba4e3685b
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
