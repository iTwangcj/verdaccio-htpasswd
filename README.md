# PPM Module For User Auth Via Htpasswd

`ppm-htpasswd` is a default authentication plugin for the [PPM](https://github.com/ppm/ppm).

> This plugin is being used as dependency after `v3.0.0-beta.x`. The `v2.x` still contains this plugin built-in.

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

## Generate htpasswd username/password combination

If you wish to handle access control using htpasswd file, you can generate
username/password combination form
[here](http://www.htaccesstools.com/htpasswd-generator/) and add it to htpasswd
file.

## How does it work?

The htpasswd file contains rows corresponding to a pair of username and password
separated with a colon character. The password is encrypted using the UNIX system's
crypt method and may use MD5 or SHA1.

## Plugin Development in ppm

There are many ways to extend [ppm](https://github.com/ppm/ppm),
currently it support authentication plugins, middleware plugins (since v2.7.0)
and storage plugins since (v3.x).
#### Useful Links
- [Plugin Development](http://www.ppm.org/docs/en/dev-plugins.html)
- [List of Plugins](http://www.ppm.org/docs/en/plugins.html)
