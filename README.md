# nginx-forward-proxy

## What is this?

A 'nginx-foward-proxy' is a so simple HTTP proxy server using the nginx.
You can easily build a HTTP proxy server using this.

## Try this container

### Requirement packages

- Docker

### Use on docker

```bash
$ docker run --rm -d -p 3128:3128 kilerkarol/nginx-forward-proxy:latest
$ curl -x http://127.0.0.1:3128 https://www.google.com
```

### Use on kubernetes

```bash
$ kubectl apply -f nginx-forward-proxy.yaml
# from another kubernetes container
curl -x http://nginx-proxy-service.default.svc.cluster.local:3128 https://www.google.com
```

## Links

- https://github.com/chobits/ngx_http_proxy_connect_module
