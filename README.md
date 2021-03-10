# Basic Monitoring Stack Setup

Sets up a basic monitoring stack including Prometheus, Alertmanager and Grafana and connects it all together.

## Usage

### Create namespace (only run if it not already exists)

```sh
kubectl create namespace monitoring
```

### Create CRDs

```sh
kubectl apply -f crds.yaml -nmonitoring
```

### Create Prometheus & Alertmanager

```sh
kubectl apply -f prometheus.yaml -nmonitoring
```

### Create Grafana

```sh
kubectl apply -f grafana.yaml -nmonitoring
```
