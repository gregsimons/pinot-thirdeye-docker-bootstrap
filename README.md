# pinot-thirdeye-docker-bootstrap

This project uses docker compose to bootstrap an apache pinot cluster with thirdeye. It builds upon the
climate change analysis demo by @kbastani [climate change analysis](https://github.com/kbastani/climate-change-analysis)
to strip out Apache superset and bootstrap a basic demo cluster with thirdeye.

## Pre-requisite

You will require docker to be setup on your machine and also a minimum memory footprint for docker of around 3gb once
you start to ingest data. This can be set by opening the docker preferences > Resources > Advanced and sliding the bar
for Memory allocation.

## Usage

Intended usage of the bootstrap is to help developers start a base cluster for building applications with Apache Pinot
in development only. **Not for production use.**

```bash
$ docker-compose up -d
$ docker-compose logs -f --tail=100
```

At this point you will be ready to access your cluster at

    [Pinot Dashboard](http://localhost:9000)
    [Thirdeye Dashboard]([http://localhost:1426/app/#/login)

Thirdeye dashboard will require you to authenticate with the credentials admin:admin
