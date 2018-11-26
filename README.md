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

You can specify an uploadable file size using the environment variable (MAX_FILE_SIZE).
To set 10MB, proceed as follows.

```
docker run -d -p 8080:8080 -e MAX_FILE_SIZE=10485760 gitbucket/gitbucket
```
