Apache Proxy build pack
========================

This is a build pack bundling Apache and mod_proxy for Heroku apps.

Configuration
-------------

The config files are bundled with the Buildpack itself:

* conf/httpd.conf

Uses the PROXY_URL config variable as the target of the reverse proxy.

Meta
----

Forked from https://github.com/brandon-rhodes/heroku-buildpack-php