# Fluentd-docker
Fluentd-docker is a project to build a custom docker image containing fluentd and several plugins.

Fluentd image with plugin installed:
- https://github.com/fluent/fluent-plugin-prometheus
- https://github.com/fluent/fluent-plugin-rewrite-tag-filter
- https://github.com/uken/fluent-plugin-elasticsearch

This image is base on https://hub.docker.com/r/fluent/fluentd/.
You can define your own config by mounting your fluentd config :

`docker run -ti -v $PWD/fluent.conf:/fluentd.conf -e FLUENTD_CONF=yours.conf`

# Release

To release a new docker image on docker hub https://hub.docker.com/r/skycirrus/fluentd-docker/, we need to create a tag on master: 

```
git checkout master
git tag v0.0.x
git push origin v0.0.x

```
