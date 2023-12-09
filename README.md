# Custom docker images

This repository creates some custom docker image.
These images will be build automatically on a weekly basis according to:
`cron: "0 20 * * 0" # UTC`

// TODO: add badges here

## Images

### Caddy with sso

This Caddy image is based on the `caddy` docker image.
Mostly for SSO (Single Sign-On) support, the following Caddy modules are installed in the base docker image:

- github.com/caddyserver/replace-response
- github.com/greenpau/caddy-security
- github.com/greenpau/caddy-trace

### Nextcloud with ffmpeg

This Nextcloud image is based on the `nextcloud:apache` docker image.
The default Nextcloud image misses the preview generation for video files, as some dependencies aren't installed.
To this this issue, the following packages are installed on top of the base docker image:

- ffmpeg
- imagemagick-common

## Usage

For each of the custom docker images, a docker-compose.yml file is added to the respective folder.
Example usage of the docker image can be seen in these files.

## FAQ

## License

MIT License, Copyright (c) 2023 Tim Klein Nijenhuis <tim@hetorus.nl>
