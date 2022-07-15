gitbucket-docker-arm64 [![default build](https://github.com/StevenMassaro/gitbucket-docker-arm64/actions/workflows/default.yml/badge.svg)](https://github.com/StevenMassaro/gitbucket-docker-arm64/actions/workflows/default.yml)
========
Docker image of GitBucket which is an open source GitHub server powered by Scala, and is compatible with arm64 platforms.

https://hub.docker.com/r/stevenmassaro/gitbucket-arm64

How to use this image
--------

```
docker run -d -p 8080:8080 stevenmassaro/gitbucket-arm64
```

Add `-p 29418:29418` option if you would like to enable SSH for repository access:

```
docker run -d -p 8080:8080 -p 29418:29418 stevenmassaro/gitbucket-arm64
```

You can also specify the data directory by `-v` option:

```
docker run -d -p 8080:8080 -v `pwd`/gitbucket:/gitbucket stevenmassaro/gitbucket-arm64
```

You can configure GitBucket via environment variables. For example, the uploadable file size can be set to 10MB as follows:

```
docker run -d -p 8080:8080 -e GITBUCKET_MAXFILESIZE=10485760 stevenmassaro/gitbucket-arm64
```

See more details about how to configure GitBucket at: https://github.com/gitbucket/gitbucket/wiki/Basic-configurations
