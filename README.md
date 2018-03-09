# Tiny SSL reverse proxy

*Tiny SSL reverse proxy* creates a SSL reverse proxy to wrap your HTTP services in HTTPS.

This is not secure at all (it doesn't even try to be) and should only be used for development and test purposes.

## Usage

Run:

    ./ssl-reverse-proxy

That's it. You don't even need to be root.

## Notes

You'll probably get this warning message at startup:

    nginx: [alert] could not open error log file: open() "/var/log/nginx/error.log" failed (2: No such file or directory)

Don't worry: that's because nginx (on which Tiny SSL reverse proxy is based) is always looking for this file in its default location, which only the root can access. This is not fatal and has not functional impact.

## License

Tiny SSL reverse proxy is copyright (C) 2018 Jérémie Roquet <jroquet@arkanosis.net> and licensed under the ISC license.
