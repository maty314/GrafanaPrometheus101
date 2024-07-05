# Basic Monitoring System with Grafana and Prometheus

This project sets up a basic monitoring system using Grafana and Prometheus with Docker.

## Instructions

1. Clone the repository.
2. Navigate to the project folder.
3. Run `docker-compose up`.
4. Access Grafana at `http://localhost:3000`

## Files

- `docker-compose.yml`: Docker Compose configuration.
- `prometheus/prometheus.yml`: Prometheus configuration.
- `grafana/provisioning/datasources/datasource.yaml`: Grafana datasource for Prometheus.
- `grafana/provisioning/dashboards/dashboard.yaml`: Grafana dashboard configuration.
- `grafana/dashboards/dashboard.yml`: Out of the box dashboard to check if Prometheus is up. 

