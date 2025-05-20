# Results

## Test environment

NGINX Plus: false

NGINX Gateway Fabric:

- Commit: 66d6f36a8896cb0991348a7acc380ff4897a7e96
- Date: 2025-05-20T17:14:57Z
- Dirty: false

GKE Cluster:

- Node count: 12
- k8s version: v1.32.3-gke.1785003
- vCPUs per node: 16
- RAM per node: 65851332Ki
- Max pods per node: 110
- Zone: us-west1-b
- Instance Type: n2d-standard-16

## Test1: Running latte path based routing

```text
Requests      [total, rate, throughput]         30000, 1000.03, 1000.01
Duration      [total, attack, wait]             30s, 29.999s, 860.394µs
Latencies     [min, mean, 50, 90, 95, 99, max]  700.394µs, 937.732µs, 918.398µs, 1.047ms, 1.092ms, 1.23ms, 14.431ms
Bytes In      [total, mean]                     4800000, 160.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```

## Test2: Running coffee header based routing

```text
Requests      [total, rate, throughput]         30000, 1000.06, 1000.03
Duration      [total, attack, wait]             29.999s, 29.998s, 912.253µs
Latencies     [min, mean, 50, 90, 95, 99, max]  729.21µs, 969.285µs, 954.2µs, 1.069ms, 1.116ms, 1.246ms, 17.953ms
Bytes In      [total, mean]                     4830000, 161.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```

## Test3: Running coffee query based routing

```text
Requests      [total, rate, throughput]         30000, 1000.02, 999.99
Duration      [total, attack, wait]             30s, 29.999s, 916.998µs
Latencies     [min, mean, 50, 90, 95, 99, max]  699.499µs, 968.324µs, 949.334µs, 1.071ms, 1.112ms, 1.23ms, 15.731ms
Bytes In      [total, mean]                     5070000, 169.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```

## Test4: Running tea GET method based routing

```text
Requests      [total, rate, throughput]         30000, 1000.04, 1000.00
Duration      [total, attack, wait]             30s, 29.999s, 983.302µs
Latencies     [min, mean, 50, 90, 95, 99, max]  701.738µs, 959.004µs, 940.79µs, 1.063ms, 1.105ms, 1.252ms, 21.194ms
Bytes In      [total, mean]                     4740000, 158.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```

## Test5: Running tea POST method based routing

```text
Requests      [total, rate, throughput]         30000, 1000.04, 1000.01
Duration      [total, attack, wait]             30s, 29.999s, 931.139µs
Latencies     [min, mean, 50, 90, 95, 99, max]  721.208µs, 948.397µs, 934.072µs, 1.053ms, 1.1ms, 1.244ms, 10.389ms
Bytes In      [total, mean]                     4740000, 158.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```
