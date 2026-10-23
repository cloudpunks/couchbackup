FROM ghcr.io/cloudpunks/alpine:3.24@sha256:7cb29c630a04ad696336943dc35fa54e1750a6fb29e99bab34dc7af644f4e900
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.19

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
