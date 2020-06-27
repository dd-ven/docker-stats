Docker Stats
========

Una solución de monitoreo para Docker hosts y contenedores con [Prometheus](https://prometheus.io/), [Grafana](http://grafana.org/), [cAdvisor](https://github.com/google/cadvisor),
[NodeExporter](https://github.com/prometheus/node_exporter) y alertas con [AlertManager](https://github.com/prometheus/alertmanager).

***Si está buscando la versión Docker Swarm, vaya a [stefanprodan/swarmprom](https://github.com/stefanprodan/swarmprom)***

## Instalar en PC

Clone este repositorio en su host Docker, cd en el directorio dockprom y ejecute compose:

````
git clone https://github.com/dd-ven/docker-stats.git
````
````
cd docker-stats
````
````
docker-compose up -d
````

Prerrequisitos:

* Docker Engine >= 1.13
* Docker Compose >= 1.11

Contenedores:

* Prometheus (metrics database) `http://<host-ip>:9090`
* Prometheus-Pushgateway (push acceptor for ephemeral and batch jobs) `http://<host-ip>:9091`
* AlertManager (alerts management) `http://<host-ip>:9093`
* Grafana (visualize metrics) `http://<host-ip>:3000`
* NodeExporter (host metrics collector)
* cAdvisor (containers metrics collector)
* Caddy (reverse proxy and basic auth provider for prometheus and alertmanager)

## Configurar Grafana

Vaya a `http://<host-ip>:3030` e inicio de sesión con el usuario ***admin*** contraseña de ***admin***.

# Creditos

Este repositorio es una copia de ``https://github.com/stefanprodan/dockprom.git`` modificada.