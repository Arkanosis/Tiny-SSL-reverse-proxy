# Tiny SSL reverse proxy [![Version](https://img.shields.io/badge/version-v0.1.1-orange.svg)](https://semver.org/spec/v2.0.0.html) [![License](http://img.shields.io/badge/license-ISC-blue.svg)](/LICENSE)

*Tiny SSL reverse proxy* creates a SSL reverse proxy to wrap your HTTP services in HTTPS.

This is not secure at all (it doesn't even try to be) and should only be used for development and test purposes.

## Usage

```console
Usage: ssl-reverse-proxy
       ssl-reverse-proxy -h | --help
       ssl-reverse-proxy --version

Options:
    -h, --help  Show this screen.
    --version   Show version.
```

In othe words, just run:

    ./ssl-reverse-proxy

And that's it. You don't even need to be root.

## Notes

You'll probably get this warning message at startup:

    nginx: [alert] could not open error log file: open() "/var/log/nginx/error.log" failed (2: No such file or directory)

Don't worry: that's because nginx (on which Tiny SSL reverse proxy is based) is always looking for this file in its default location, which only the root can access. This is not fatal and has not functional impact.

## License

Tiny SSL reverse proxy is copyright (C) 2018-2022 Jérémie Roquet <jroquet@arkanosis.net> and licensed under the ISC license.
