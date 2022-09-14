## 문제
- `prometheus: error: unknown short flag '-c'`

## 해결
```yml
version: '3'
services:
  grafana:
    ports:
      - "3333:3000"
    volumes:
      - /var/lib/grafana
    links:
      - prometheus
    image: grafana/grafana
  prometheus:
    ports:
      - "9999:9090"
    volumes:
      - ./prometheus.yml:/etc/prometheus/prometheus.yml
    command:
      - '--config.file=/etc/prometheus/prometheus.yml' ⭐ - 이거 2개 작성해야됨!
    image: prom/prometheus
```
