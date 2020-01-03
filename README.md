gitbucket-docker
========
Docker image of GitBucket which is an open source GitHub server powered by Scala

[![Docker build](http://dockeri.co/image/gitbucket/gitbucket)](https://registry.hub.docker.com/u/gitbucket/gitbucket/)

How to use this image
--------

```
docker run -d -p 8080:8080 gitbucket/gitbucket
```

Add `-p 29418:29418` option if you would like to enable SSH for repository access:

```
docker run -d -p 8080:8080 -p 29418:29418 gitbucket/gitbucket
```

You can also specify the data directory by `-v` option:

```
docker run -d -p 8080:8080 -v `pwd`/gitbucket:/gitbucket gitbucket/gitbucket
```

You can configure GitBucket via environment variables. For example, the uploadable file size can be set to 10MB as follows:

```
docker run -d -p 8080:8080 -e GITBUCKET_MAXFILESIZE=10485760 gitbucket/gitbucket
```

See more details about how to configure GitBucket at: https://github.com/gitbucket/gitbucket/wiki/Basic-configurations
