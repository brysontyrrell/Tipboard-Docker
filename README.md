# Tipboard-Docker

Tipboard-Docker allows you to deploy a containerized version of the [Tipboard](https://github.com/allegro/tipboard) application using Docker-Compose. Three containers are launched when you run `docker-compose up`:

* Redis
* Tipboard (the web app)
* Nginx

## Clone and Replace

Clone the repository and customize your dashboard within the `/tipboard/files/` directory.

The default `layout_config.yaml` file can be updated or replaced with your own layout file(s). Within `settings-local.py` update the `API_KEY` and `PROJECT_NAME` values.

(**Do not change the `REDIS_HOST` setting!**)

To learn more about how to customize the layout, or built multiple layouts and set automatic rotation between them, head over to Tipboard's official docs:

[http://tipboard.readthedocs.io/en/latest/configuration.html](http://tipboard.readthedocs.io/en/latest/configuration.html)

## Build and Deploy the Application

```
$ eval $(docker-machine env <docker-host>)
$ docker-compose build
...
$ docker-compose up -d
```

## Update Tiles with the API

Head back to the Tipboard docs to learn about updating your tiles using the application's built-in API:

[http://tipboard.readthedocs.io/en/latest/api.html](http://tipboard.readthedocs.io/en/latest/api.html)