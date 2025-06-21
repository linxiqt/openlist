### openlist
`docker-compose.yml`国内网络部署
```
services:
  openlist:
    image: ghcr.nju.edu.cn/linxiqt/openlist:latest
    container_name: openlist
    volumes:
      - ./openlist:/opt/openlist/data
    ports:
      - 5244:5244
    environment:
      - PUID=0
      - PGID=0
      - UMASK=022
    restart: unless-stopped
```

---

`docker-compose.yml`国外网络部署
```
services:
  openlist:
    image: ghcr.io/linxiqt/openlist:latest
    container_name: openlist
    volumes:
      - ./openlist:/opt/openlist/data
    ports:
      - 5244:5244
    environment:
      - PUID=0
      - PGID=0
      - UMASK=022
    restart: unless-stopped
```
---

- [官网文档](https://docs.openlist.team/zh/guide/install/docker.html)
