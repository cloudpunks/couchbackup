FROM ghcr.io/cloudpunks/alpine:3.19@sha256:3b8f511db2c0caf9795a757a7ce787549403708202c136aeb096dbe38aa461ba
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.17

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
