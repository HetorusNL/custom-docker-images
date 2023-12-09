# Custom docker images

This repository creates some custom docker image.

// TODO: add badges here

## Images

### Nextcloud with ffmpeg

This Nextcloud image is based on the `nextcloud:apache` docker image.
The default Nextcloud image misses the preview generation for video files, as some dependencies aren't installed.
To this this issue, the following packages are installed on top of the base docker image:

- imagemagick-common
- ffmpeg

### Caddy with sso

This Caddy image is based on the `caddy` docker image.
Mostly for SSO (Single Sign-On) support, the following Caddy modules are installed in the base docker image:

- github.com/greenpau/caddy-trace
- github.com/greenpau/caddy-security
- github.com/caddyserver/replace-response

## Usage

For each of the custom docker images, a docker-compose file is added to the respective folder.
Example usage of the docker image can be seen in these files.

## FAQ

## License

MIT License, Copyright (c) 2023 Tim Klein Nijenhuis <tim@hetorus.nl>
