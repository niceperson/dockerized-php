# Web Server

Nginx & PHP 7 web server.
[`inspired by Neo Ighodaro`](https://github.com/neoighodaro)

# How To

- copy the `docker-compose.yml` to the project root folder
- pay attention to the docker-composer settings. the current one is meant to be used with [playground](https://github.com/niceperson/playground)
- for standalone, please bind the app port with host port
``` yml
    ports:
      - "8080:80" #host:app

```


### Args

Here are some args

- `NGINX_HTTP_PORT` - HTTP port. Default: `80`.
- `NGINX_HTTPS_PORT` - HTTPS port. Default: `443`.
- `PHP_VERSION` - The PHP version to install. Supports: `7.4`. Default: `7.4`.
- `ALPINE_VERSION` - The Alpine version. Supports: `3.9`. Default: `3.9`.

### Environment Variables

Here are some configurable environment values.

- `WEBROOT` – Path to the web root. Default: `/var/www`
- `WEBROOT_PUBLIC` – Path to the web root. Default: `/var/www/public`
- `COMPOSER_DIRECTORY` - Path to the `composer.json` containing directory. Default: `/var/www`.
- `COMPOSER_INSTALL_ON_BUILD` - Should `composer install` run on build. Default: `0`.
- `LARAVEL_APP` - Is this a Laravel application. Default `0`.
- `RUN_LARAVEL_SCHEDULER` - Should the Laravel scheduler command run. Only works if `LARAVEL_APP` is `1`. Default: `0`.
- `RUN_LARAVEL_MIGRATIONS_ON_BUILD` - Should the migrate command run during build. Only works if `LARAVEL_APP` is `1`. Default: `0`.
- `PRODUCTION` – Is this a production environment. Default: `0`
- `PHP_MEMORY_LIMIT` - PHP memory limit. Default: `128M`
- `PHP_POST_MAX_SIZE` - Maximum POST size. Default: `50M`
- `PHP_UPLOAD_MAX_FILESIZE` - Maximum file upload file. Default: `10M`.
