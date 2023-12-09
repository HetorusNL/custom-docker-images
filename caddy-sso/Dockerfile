FROM caddy:builder AS builder

RUN xcaddy build \
    --with github.com/caddyserver/replace-response \
    --with github.com/greenpau/caddy-security \
    --with github.com/greenpau/caddy-trace

FROM caddy

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

# add the container labels
LABEL org.label-schema.vcs-ref=$VCS_REF
LABEL org.label-schema.vcs-url=https://github.com/HetorusNL/custom-docker-images
LABEL org.opencontainers.image.authors=tim@hetorus.nl
LABEL org.opencontainers.image.source=https://github.com/HetorusNL/custom-docker-images
LABEL org.opencontainers.image.description="caddy docker image with the greenpau/caddy-security (SSO) modules installed"
LABEL org.opencontainers.image.licenses=MIT
