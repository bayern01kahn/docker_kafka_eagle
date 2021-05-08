升级 kafka-eagle 版本到dockerhub.

1.进入docker-kafka-eagle 项目目录, 修改dockerfile中 version 为当前最新kafka-eagle版本 

2.本地构建新版本的image.  并指定新的版本号 -t name:version

```
docker build . -t kafka-eagle:2.0.5
```

3.登录dockerhub

```
docker login
```

4.查看新生成的image, 并复制imageID

```
docker images
```

5.将该image 打上对应repo 的tag. 可以完成后 docker image 查看

```
docker tag 02496ed3e4d2 bayern01kahn/kafka-eagle:2.0.5
```

6.push 到 docker hub

```
docker push bayern01kahn/kafka-eagle:2.0.5
```



