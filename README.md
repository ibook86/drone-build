# Drone Enterprise Docker镜像

> The Enterprise Edition is free for organizations with under $1 million US dollars in annual gross revenue.

## 注意

**该Docker镜像仅供学习研究使用，用于生产环境请慎重选择！**

## 使用

`docker pull ibook163/drone:latest`

```shell
docker run \
  --volume=/var/lib/drone:/data \
  --env=DRONE_GITHUB_CLIENT_ID={{DRONE_GITHUB_CLIENT_ID}} \
  --env=DRONE_GITHUB_CLIENT_SECRET={{DRONE_GITHUB_CLIENT_SECRET}} \
  --env=DRONE_RPC_SECRET={{DRONE_RPC_SECRET}} \
  --env=DRONE_SERVER_HOST={{DRONE_SERVER_HOST}} \
  --env=DRONE_SERVER_PROTO={{DRONE_SERVER_PROTO}} \
  --publish=80:80 \
  --publish=443:443 \
  --restart=always \
  --detach=true \
  --name=drone \
  ibook163/drone:latest
```

## 参见：
https://docs.drone.io/server/provider/github/

https://docs.drone.io/enterprise/
