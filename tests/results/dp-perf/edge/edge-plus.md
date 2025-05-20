# Results

## Test environment

NGINX Plus: true

NGINX Gateway Fabric:

- Commit: 66d6f36a8896cb0991348a7acc380ff4897a7e96
- Date: 2025-05-20T17:14:57Z
- Dirty: false

GKE Cluster:

- Node count: 12
- k8s version: v1.32.3-gke.1785003
- vCPUs per node: 16
- RAM per node: 65851340Ki
- Max pods per node: 110
- Zone: us-west1-b
- Instance Type: n2d-standard-16

## Test1: Running latte path based routing

```text
Requests      [total, rate, throughput]         29999, 1000.00, 999.97
Duration      [total, attack, wait]             30s, 29.999s, 791.665µs
Latencies     [min, mean, 50, 90, 95, 99, max]  675.837µs, 931.514µs, 900.171µs, 1.028ms, 1.083ms, 1.294ms, 23.359ms
Bytes In      [total, mean]                     4739842, 158.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:29999  
Error Set:
```

## Test2: Running coffee header based routing

```text
Requests      [total, rate, throughput]         30000, 1000.03, 1000.00
Duration      [total, attack, wait]             30s, 29.999s, 829.798µs
Latencies     [min, mean, 50, 90, 95, 99, max]  699.872µs, 954.024µs, 924.522µs, 1.058ms, 1.106ms, 1.279ms, 207.596ms
Bytes In      [total, mean]                     4770000, 159.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```

## Test3: Running coffee query based routing

```text
Requests      [total, rate, throughput]         30000, 1000.06, 1000.02
Duration      [total, attack, wait]             29.999s, 29.998s, 1.166ms
Latencies     [min, mean, 50, 90, 95, 99, max]  668.81µs, 960.172µs, 941.911µs, 1.07ms, 1.118ms, 1.291ms, 11.068ms
Bytes In      [total, mean]                     5010000, 167.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```

## Test4: Running tea GET method based routing

```text
Requests      [total, rate, throughput]         29999, 1000.00, 999.97
Duration      [total, attack, wait]             30s, 29.999s, 1.003ms
Latencies     [min, mean, 50, 90, 95, 99, max]  705.934µs, 980.306µs, 962.806µs, 1.1ms, 1.159ms, 1.374ms, 18.465ms
Bytes In      [total, mean]                     4679844, 156.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:29999  
Error Set:
```

## Test5: Running tea POST method based routing

```text
Requests      [total, rate, throughput]         30000, 1000.02, 1000.00
Duration      [total, attack, wait]             30s, 29.999s, 843.32µs
Latencies     [min, mean, 50, 90, 95, 99, max]  727.931µs, 984.586µs, 965.124µs, 1.107ms, 1.164ms, 1.329ms, 13.12ms
Bytes In      [total, mean]                     4680000, 156.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```
