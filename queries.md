# PromQL Queries used in Grafana Dashboard

## CPU Usage
rate(node_cpu_seconds_total{mode!="idle"}[5m])

## Memory Usage
node_memory_MemTotal_bytes - node_memory_MemAvailable_bytes

## Disk Space Usage
100 - (node_filesystem_avail_bytes{mountpoint="/"} * 100 / node_filesystem_size_bytes{mountpoint="/"})