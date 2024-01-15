# Portainer HTTPS template for VPS/VDS
A template for rapid deployment of Portainer on shared hosting. It uses:
- [Portainer Community Edition (CE)](https://www.portainer.io/) - A lightweight service delivery platform for containerized applications that can be used to manage Docker, Swarm, Kubernetes and ACI environments
- [nginx-proxy](https://github.com/nginx-proxy/nginx-proxy) - Automated nginx proxy for Docker containers using docker-gen
- [acme-companion](https://github.com/nginx-proxy/acme-companion) - Automated ACME SSL certificate generation for nginx-proxy

# How to use
1. Clone this repo to your VPS hosting
    ```shell
    git clone https://github.com/zakharsk/portainer-https.git && cd portainer-https
    ```
2. Create `.env` file
    ```shell
    cp example.env .env && vim .env
    ```
3. Put your values for `PORTAINER_DOMAIN` and `PORTAINER_DOMAIN_EMAIL`. `PORTAINER_DOMAIN` **without** specifying the `http/https` protocol and **without** a `/` at the end. 
4. Start you container
    ```bash
    docker compose up --force-recreate --detach
    ```
5. Open the `PORTAINER_DOMAIN` address in your favorite browser. 
6. To stop
    ```bash
    docker compose down
    ```