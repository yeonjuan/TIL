# 도커 컨테이너 삭제

`docker rm` 커맨드로 컨테이너를 삭제할 수 있다.

```
docker rm {CONTAINER_ID}

docker rm {CONTAINER_NAME}
```

실행중인 컨테이너에 사용하면 에러가 발생한다.
그땐 `docker stop` 으로 컨테이너를 중지하고 삭제할 수 있다.

```
docker stop {CONTAINER_ID}

docker stop {CONTAINER_NAME}
```
