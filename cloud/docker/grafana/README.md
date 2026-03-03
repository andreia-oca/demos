# Deploy Grafana & Prometheus

```bash
docker-compose up -d
```

Verify deployment:

```bash
docker ps -a
docker logs prometheus
docker network ls
docker inspect grafana_monitoring
```

To connect to the GUI use `ssh -L port:guest_ip:guest_port host`.
Now you can access Grafana by browsing to `https://localhost:3000`.

Add a new Data Source - prometheus . Set the Prometheus server URL to `http://prometheus:9090` (we can do that thanks to docker and monitoring network).

Import a new dashboard - ID is 1860 - https://grafana.com/grafana/dashboards/1860-node-exporter-full/.
