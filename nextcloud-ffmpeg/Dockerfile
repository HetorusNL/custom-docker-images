FROM nextcloud:apache

RUN apt-get update && apt-get install -y \
    ffmpeg \
    imagemagick-common \
    && rm -rf /var/lib/apt/lists/*

# add the container labels
LABEL org.label-schema.vcs-ref=$VCS_REF
LABEL org.label-schema.vcs-url=https://github.com/HetorusNL/custom-docker-images
LABEL org.opencontainers.image.authors=tim@hetorus.nl
LABEL org.opencontainers.image.source=https://github.com/HetorusNL/custom-docker-images
LABEL org.opencontainers.image.description="nextcloud:apache docker image with ffmpeg and imagemagick-common preinstalled"
LABEL org.opencontainers.image.licenses=MIT
