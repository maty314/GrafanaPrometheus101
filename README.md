# Basic Monitoring System with Grafana and Prometheus

This project sets up a monitoring system using Grafana and Prometheus with Docker. It includes CI/CD configuration with GitHub Actions to ensure the services are always up-to-date and functioning correctly.

## Features

- **Prometheus**: Collects and stores metrics.
- **Grafana**: Visualizes the metrics collected by Prometheus.
- **Node Exporter**: Provides OS metrics for Prometheus.
- **Alertmanager**: Manages alerts sent by Prometheus.
- **CI/CD with GitHub Actions**: Automates the deployment and testing of the system.

## Prerequisites

- Docker and Docker Compose installed on the system.
- A Docker Hub account.
- Environment variables configured for Docker Hub and Grafana authentication.

## Configuration

### Environment Variables

Create a `.env` file in the root of the project with the following variables:

- `GF_SECURITY_ADMIN_USER=admin`

- `GF_SECURITY_ADMIN_PASSWORD=admin`

## Instructions

1. Clone the repository.
2. Navigate to the project folder.
3. Create a .env file in the root directory with the necessary environment variables.
4. Run docker-compose up -d to start the services.
5. Access Prometheus at http://localhost:9090.
6. Access Grafana at http://localhost:3000 and use the credentials defined in the .env file.

## CI/CD

The CI/CD pipeline is defined in .github/workflows/ci-cd.yml and performs the following actions:

- Builds and pushes Docker images.
- Deploys the system using Docker Compose.
- Checks that the services are running correctly.
- Checks that the out of the box dashboards are working with data from the datasource(prometheus).


### Setting Up GitHub Secrets

To set up GitHub secrets for the CI/CD pipeline, follow these steps:

1. Navigate to your forked repository on GitHub.
2. Go to **Settings** > **Secrets and variables** > **Actions**.
3. Add the following secrets:
   - `DOCKER_USERNAME`: Your Docker Hub username.
   - `DOCKER_PASSWORD`: Your Docker Hub password.
   - `GF_SECURITY_ADMIN_USER`: Your Grafana admin username.
   - `GF_SECURITY_ADMIN_PASSWORD`: Your Grafana admin password.


## Monitoring

- Prometheus: Access Prometheus at http://localhost:9090.
- Grafana: Access Grafana at http://localhost:3000 and use the credentials defined in the .env file.

## Contributions

Contributions are welcome. Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License.

