# ssr-docker
```bash
docker run \
--name=shadowsocksr-client \
--restart=unless-stopped \
--network=host \
--detach --volume /var/www/shadowsocksr-docker/config.json:/etc/shadowsocksr/config.json \
--volume /var/www/shadowsocksr-docker/entry-point.sh:/etc/shadowsocksr/entry-point.sh \
python:3.8-alpine /bin/sh -c "/etc/shadowsocksr/entry-point.sh client"
```
