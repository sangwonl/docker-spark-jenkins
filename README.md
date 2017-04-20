`Dockerfile` in this repository refers to https://github.com/jenkinsci/docker for `jenkins`

## Pre-requisite

There should be a bridge network named as `hadoop` where hadoop cluster runs on.

```
$ docker network create -d bridge hadoop
```

## Run spark integrated jenkins container in hadoop network

```
$ docker run -it --network hadoop --env-file hadoop.env -p 8080:8080 sangwonl/hadoop-spark-jenkins
```