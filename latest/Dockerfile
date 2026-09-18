FROM ghcr.io/cloudpunks/alpine:3.24@sha256:d1f1c104aabb0279a75d2e8feb74a1f01fd75ae1ac7337a1a113ae5d8ddb289f
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.19

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
