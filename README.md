# vps-traefik

This repo contains docker-compose that runs Traefik on a server.

## How to run this

- Create `.env` file - see `.env.example`

- Create `acme.json` file and give it permissions:

```sh
touch acme.json
chmod 600 acme.json
```

- Create some hashed password - example:

```sh
sudo apt install apache2-utils
htpasswd -nb admin your_password
```

- Create `usersfile.txt` with the hashed password

- Install [Grafana Loki Docker driver client](https://grafana.com/docs/loki/latest/send-data/docker-driver/) for logging

- Run docker compose:

```sh
docker compose up
```
