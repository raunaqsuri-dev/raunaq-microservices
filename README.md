# Raunaq Microservices Starter

A ready-to-run skeleton for a Spring Boot microservices playground.

Includes:
- docker-compose infra (Postgres, Kafka+Zookeeper, Prometheus, Grafana, Zipkin)
- parent Maven POM (multi-module ready)
- repo hygiene (.gitignore, .editorconfig)
- docs folder placeholder

## Quick start
1) Unzip, open a terminal in the folder, then:
```bash
docker compose up -d
```

2) Verify infra:
- Prometheus → http://localhost:9090
- Grafana → http://localhost:3000  (user: admin / pass: admin)
- Zipkin → http://localhost:9411
- Postgres → localhost:5432 (msuser/mspass)
- Kafka broker (internal) → kafka:9092 (via Docker network), host port 9092 exposed

3) Next steps (Day 1):
- Create your first service (e.g., `catalog-service/`) using Spring Initializr
- Add the module to the root `pom.xml` under `<modules>`
- Run your service and start experimenting
