# s6 +  snooze base image

[![Build Status](https://travis-ci.org/coaxial/docker-s6-snooze.svg?branch=master)](https://travis-ci.org/coaxial/docker-s6-snooze) [![Image Size](https://images.microbadger.com/badges/image/coaxial/s6-snooze.svg)](https://microbadger.com/images/coaxial/s6-snooze "Get your own image badge on microbadger.com")

This is a Docker base image bundling [s6-overlay](https://github.com/just-containers/s6-overlay) and [snooze](https://github.com/chneukirchen/snooze) (as an alternative to cron).

The image is rebuilt whenever its base distribution image is.

## Usage

You'd typically have a Dockerfile like this:

```
FROM coaxial/s6-snooze

COPY root/ /

ENTRYPOINT ["/init"]  # don't override the entrypoint, it starts s6-overlay
```

See the s6-overlay repo and s6 docs to setup your services and your `root/` directory.

## Issues

I will consider adding other distributions and architecture as they are requested (open an issue) or as I need them.
