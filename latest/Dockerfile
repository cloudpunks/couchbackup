FROM ghcr.io/cloudpunks/alpine:3.24@sha256:bacb232473dfec7a700675b3e139e3944ad3fb26f27e59a63b86962dd7e279af
ENTRYPOINT [""]

# renovate: datasource=npm depName=@cloudant/couchbackup
ENV COUCHBACKUP_VERSION=2.11.19

RUN apk update && \
  apk upgrade && \
  apk add nodejs npm git jq curl && \
  npm install --global \
    @cloudant/couchbackup@${COUCHBACKUP_VERSION} && \
  rm -rf /var/cache/apk/*
