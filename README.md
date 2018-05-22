# S6 Snooze base image

This is a Docker base image bundling [S6 overlay](https://github.com/just-containers/s6-overlay) and [Snooze](https://github.com/chneukirchen/snooze) (as an alternative to cron).

The image is rebuilt whenever its base distribution image is.

## Usage

You'd typically have a Dockerfile like this:

```
FROM coaxial/s6-snooze

COPY root /

CMD ["/init"]  # do not change this, it starts s6
```

cf the s6-overlay repo for instructions on how to use s6 within a container, and how to define your services.

As to what goes into `root/`, it is explained on the s6-overlay repo.

## Flavours

- `alpine`

## Issues

I will consider adding other distributions and architecture as they are requested or as I need them.
