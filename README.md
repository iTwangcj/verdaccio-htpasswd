# PPM Module For User Auth Via Htpasswd

`ppm-htpasswd` is a default authentication plugin for the [PPM](https://github.com/ppm/ppm).

> This plugin is being used as dependency after `v1.0.0`.

## Install

As simple as running:

    $ npm install -g ppm-htpasswd

## Configure

    auth:
        htpasswd:
            file: ./htpasswd
            # Maximum amount of users allowed to register, defaults to "+infinity".
            # You can set this to -1 to disable registration.
            #max_users: 1000

## Logging In

To log in using NPM, run:

```
    npm adduser --registry  https://your.registry.local
```

