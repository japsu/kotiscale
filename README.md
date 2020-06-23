# Kotiscale

Prometheus + Grafana + TimescaleDB + Cozify = ?

## Getting started

Create a file called `.env` with the following contents:

    POSTGRES_USERNAME=kotiscale
    POSTGRES_PASSWORD=<make up a secure password>
    GRAFANA_USERNAME=kotiscale
    GRAFANA_PASSWORD=<make up a secure password>

Start the services:

    git submodule update --init
    docker-compose up

Access the services:

* **Prometheus**: [localhost:9090](http://localhost:9090)
* **Alertmanager**: [localhost:9093](http://localhost:9093)
* **Grafana**: [localhost:3000](http://localhost:3000)
  * use `GRAFANA_USERNAME/GRAFANA_PASSWORD` set above
