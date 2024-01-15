# portainer-https
A template for rapid deployment of Portainer on shared hosting.

```bash
git clone https://github.com/zakharsk/portainer-https.git && cd portainer-https
cp example.env .env
vim .env
```

Fill `PORTAINER_DOMAIN` and `PORTAINER_DOMAIN_EMAIL`.


For run:
```bash
docker compose up --force-recreate --detach
```

For stop:
```bash
docker compose down
```