gitbucket-docker
========
GitBucket is an open-source GitHub clone powered by Scala.

How to use this image
--------

```
docker run -d -p 8080:8080 takezoe/gitbucket
```

Add `-p 29418:29418` option if you would like to enable SSH for repository access:

```
docker run -d -p 8080:8080 -p 29418:29418 takezoe/gitbucket
```

You can also specify the data directory by `-v` option:

```
docker run -d -p 8080:8080 -v `pwd`/gitbucket:/gitbucket takezoe/gitbucket
```
