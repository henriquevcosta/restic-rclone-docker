A clone of tofran/restic-rclone-docker. No relevant changes added apart from pushing to my registry and having control of the changes.

# restic-rclone docker images

[![Automatic builds badge](https://github.com/henriquevcosta/restic-rclone-docker/actions/workflows/trigger-build.yaml/badge.svg)](https://github.com/henriquevcosta/restic-rclone-docker/actions/workflows/trigger-build.yaml)
[![Docker image size](https://img.shields.io/docker/image-size/henriquevcosta/restic-rclone?sort=date)][DockerHub]
[![Docker pulls](https://img.shields.io/docker/pulls/henriquevcosta/restic-rclone)][DockerHub]

Always up-to-date minimal Alpine multi-arch images, with **Restic** and **Rclone** tagged for each
version combination.

[henriquevcosta/restic-rclone @ Docker Hub][DockerHub]

[henriquevcosta/restic-rclone @ GitHub container registry][GHCR]


## Tags

Images are tagged with a combination of Restic and Rclone tags, in the format:
`{RESTIC_TAG}_{RCLONE_TAG}`.

Example tags: `latest_latest`, `0.16.0_1.64.0`, `latest_1.64.0`, `0.16.0_latest`.

The latest 4 images from both upstreams are maintained. Image building is automatic, via [GitHub actions](https://github.com/henriquevcosta/restic-rclone-docker/actions).

## Architecture support

Images are built for the following architectures:
`linux/386`, `linux/amd64`, `linux/arm`, `linux/arm64`

## Usage

```sh
# Optionally, first pull the image from your favourite registry:
$ docker pull henriquevcosta/restic-rclone:0.15.1_1.61.1
#  or
$ docker pull ghcr.io/henriquevcosta/restic-rclone:0.15.1_1.61.1

# Run it:
$ docker run henriquevcosta/restic-rclone:0.15.1_1.61.1 -v
#  or
$ docker run ghcr.io/henriquevcosta/restic-rclone:0.15.1_1.61.1 -v
# > restic 0.15.1 compiled with go1.19.5 on linux/amd64
```

`restic` is the default entrypoint.

[DockerHub]: https://hub.docker.com/r/henriquevcosta/restic-rclone
[GHCR]: https://github.com/henriquevcosta/restic-rclone-docker/pkgs/container/restic-rclone
