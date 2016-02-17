Apache Proxy build pack
========================

This is a build pack bundling Apache and mod_proxy for Heroku apps.

Configuration
-------------

The config files are bundled with the Buildpack itself:

* conf/httpd.conf

You can specify additional config files in your app - put any number of `.conf` files inside a `conf` directory 
in the root of your application repository and they will be included when Apache starts. You could include additional 
libraries in your app repository if you need to load modules.

The document root is set to `/app/www` - the default configuration won't ever display anything from this directory - but if 
you want to include files for the document root you can include a `www` directory in your app.

The detect phase of the buildpack will look for either a file named `proxy_on` in the root of an app, or for the
aforementioned `conf` directory to exist in order to detect it as a candidate for this buildpack.

Set the PROXY_URL config variable on your app to set the target for the reverse proxy.

Meta
----

Forked from https://github.com/brandon-rhodes/heroku-buildpack-php