Caddyfile
========

```bash
# 32bit
DOWNLOAD_URL='https://caddyserver.com/download/linux/386?plugins=tls.dns.cloudflare&license=personal&telemetry=off'
# 64bit
DOWNLOAD_URL='https://caddyserver.com/download/linux/amd64?plugins=tls.dns.cloudflare&license=personal&telemetry=off'

rm -f /usr/local/bin/caddy
curl "$DOWNLOAD_URL" | tar -zxf - -C /usr/local/bin caddy
setcap cap_net_bind_service=+ep /usr/local/bin/caddy
```

###### Reference
- https://github.com/mholt/caddy/tree/master/dist/init/linux-upstart
