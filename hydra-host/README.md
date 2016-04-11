# Hydra Dockerfile

**Minimal** docker with hydra-host


### Build image

```
docker build -t hydra-host .
```

### Run container

```
docker run -ti --name hydra-host -v /etc/timezone:/etc/timezone:ro --link rethinkdb:rethinkdb -p 4443:4443 -p 443:443 -e DATABASE_URL=rethinkdb://rethinkdb -e JWT_PUBLIC_KEY=/aresdenstudios/jwt/rs256-public.pem -e JWT_PRIVATE_KEY=/aresdenstudios/jwt/rs256-private.pem -e TLS_CERT=/aresdenstudios/tls/tls-cert.pem -e TLS_KEY=/aresdenstudios/tls/tls-key.pem hydra-host
```

```

