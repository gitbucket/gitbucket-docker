gitbucket-docker [![default build](https://github.com/gitbucket/gitbucket-docker/actions/workflows/default.yml/badge.svg)](https://github.com/gitbucket/gitbucket-docker/actions/workflows/default.yml) [![nightly build](https://github.com/gitbucket/gitbucket-docker/actions/workflows/nightly.yml/badge.svg)](https://github.com/gitbucket/gitbucket-docker/actions/workflows/nightly.yml)
========
Docker image of GitBucket which is an open source GitHub server powered by Scala

How to use this image
--------

```
docker run -d -p 8080:8080 ghcr.io/gitbucket/gitbucket
```

Add `-p 29418:29418` option if you would like to enable SSH for repository access:

```
docker run -d -p 8080:8080 -p 29418:29418 ghcr.io/gitbucket/gitbucket
```

You can also specify the data directory by `-v` option:

```
docker run -d -p 8080:8080 -v `pwd`/gitbucket:/gitbucket ghcr.io/gitbucket/gitbucket
```

You can configure GitBucket via environment variables. For example, the uploadable file size can be set to 10MB as follows:

```
docker run -d -p 8080:8080 -e GITBUCKET_MAXFILESIZE=10485760 ghcr.io/gitbucket/gitbucket
```

See more details about how to configure GitBucket at: https://github.com/gitbucket/gitbucket/wiki/Basic-configurations
