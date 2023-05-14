# NGI Analytics Stack

Matomo and MariaDB with support for optout and do-not-track for users' privacy

## Requirements

- Docker
- Docker Compose
- A discourse installation deployed via docker

## Setup

- Replace `PASSWORD_PLACEHOLDER` in `db.env` and `docker-compose.yaml`
- Replace the content of `ssl-certs/ssl.crt` and `ssl-certs/ssl.key` with valid ssl certificates
- Replace `A_VALID_PORT` in `docker-compose.yaml` with a valid port not used already in the host for something else

## Deploy

To deploy the stack simply move into the directory root of this project and run `docker compose up -d`

## Post Deployment

- Access the Matomo website using the domain chosen in `matomo.conf`, let's assume `https://matomo.netgamers.it:443`
- Follow the wizard to complete the installation.
- Install the component [Matomo Analytics](https://meta.discourse.org/t/matomo-analytics/33090) in Discourse following the instructions

## Logs

You can check the logs with `docker compose logs --follow`