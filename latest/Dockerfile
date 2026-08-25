FROM ghcr.io/cloudpunks/alpine:3.19@sha256:c14e9b97ad8994e4ddcd05d5110856994c06ac28a35f2bd434e858c1e0bd5b92
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.19

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
