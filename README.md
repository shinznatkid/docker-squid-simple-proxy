# Minimal Squid as a Proxy

## Quick instructions:

```bash
docker run --name squid_proxy -d --restart=always --publish 3128:3128 -e HTTP_PORT=0.0.0.0:3128 --volume /var/spool/squid shinznatkid/squid
```

## Run Squid with a basic HTTP authentication

We are going to use "ncsa_auth" that allows Squid to read and authenticate user and password information from an NCSA httpd-style password file when using basic HTTP authentication.

```bash
docker run --name squid_proxy -d --restart=always --publish 3128:3128 -e SQUID_USER=qwerty -e SQUID_PASS=iddqd -e HTTP_PORT=0.0.0.0:3128 --volume /var/spool/squid shinznatkid/squid
```
