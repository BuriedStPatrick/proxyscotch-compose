# Proxyscotch Docker Compose File

Run Proxyscotch inside Docker without the need to install it directly. Requires Docker Compose.

Simply run the following to start the service:

```bash
docker compose up -d
```

It will automatically start whenever you start the Docker service.

## Linux

If you want to run requests against the `host.docker.internal` Docker loop back, you need to add the following to your `/etc/hosts` file:

```.
127.0.0.1   host.docker.internal
127.0.0.1   host-gateway
```

I've already set up the `docker-compose.yaml` file to ensure the Proxyscotch instance runs on the host port. Please note, every time you want to call `localhost` from Hoppscotch running through this proxy, you instead want to run it through `host.docker.internal`. I'm not a network person, but this seems to always work at least.
