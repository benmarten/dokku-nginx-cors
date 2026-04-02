# Dokku plugin nginx-cors

Easily enable NGINX CORS.

### Install

```shell
dokku plugin:install https://github.com/USMortality/dokku-nginx-cors.git nginx-cors
```

To validate if it is working you can simply check the `access-control-allow-origin`. You can
that easily with `curl` from the command line:

```shell
curl -I -X GET http://YOURAMAZINAPP.DOMAIN.EXT/
```

### Quick start

Enable nginx CORS

```shell
dokku nginx-cors:enable MYAPP
```

Set a specific origin instead of `*`

```shell
dokku nginx-cors:set-origin MYAPP https://onyx.orthorobot.com
```

Set multiple allowed origins (comma-separated)

```shell
dokku nginx-cors:set-origin MYAPP "https://onyx.orthorobot.com,https://staging.viewtlab.com,https://test.viewtlab.com,https://test.v2.viewtlab.com"
```

Clear custom origin and go back to `*`

```shell
dokku nginx-cors:clear-origin MYAPP
```

Disable nginx cache for your app

```shell
dokku nginx-cors:disable MYAPP
```
