# Kotiscale HomeOps Platform

Prometheus + Grafana + TimescaleDB + Cozify = ?

## Getting started

Create a file called `.env` with the following contents:

    POSTGRES_USERNAME=kotiscale
    POSTGRES_PASSWORD=<make up a secure password>
    GRAFANA_USERNAME=kotiscale
    GRAFANA_PASSWORD=<make up a secure password>

If you want Cozify temperatures to work, authenticate to Cozify Cloud _outside_ the container:

    pip3 install cozify
    python3 -c 'from cozify import cloud; cloud.authenticate()'

Start the services:

    git submodule update --init
    docker-compose up

Access the services:

* **Prometheus**: [localhost:9090](http://localhost:9090)
* **Alertmanager**: [localhost:9093](http://localhost:9093)
* **Grafana**: [localhost:3000](http://localhost:3000)
  * use `GRAFANA_USERNAME/GRAFANA_PASSWORD` set above

## TODO

* [ ] Provision data sources and dashboards at cold startup (currently requires clicking)
* [ ] Ship logs to Loki (Loki and Promtail set up but currently not receiving logs)
* [ ] Toss Cozify at the marine birdlife and set up something more reasonable (it sucks :)
