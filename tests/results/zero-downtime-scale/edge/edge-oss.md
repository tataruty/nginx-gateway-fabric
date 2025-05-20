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

## One NGINX Pod runs per node Test Results

### Scale Up Gradually

#### Test: Send https /tea traffic

```text
Requests      [total, rate, throughput]         30000, 100.00, 100.00
Duration      [total, attack, wait]             5m0s, 5m0s, 1.079ms
Latencies     [min, mean, 50, 90, 95, 99, max]  656.562µs, 1.243ms, 1.194ms, 1.385ms, 1.475ms, 1.856ms, 218.579ms
Bytes In      [total, mean]                     4595884, 153.20
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```

![gradual-scale-up-affinity-https-oss.png](gradual-scale-up-affinity-https-oss.png)

#### Test: Send http /coffee traffic

```text
Requests      [total, rate, throughput]         30000, 100.00, 100.00
Duration      [total, attack, wait]             5m0s, 5m0s, 1.11ms
Latencies     [min, mean, 50, 90, 95, 99, max]  660.196µs, 1.214ms, 1.182ms, 1.366ms, 1.446ms, 1.83ms, 209.558ms
Bytes In      [total, mean]                     4776017, 159.20
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```

![gradual-scale-up-affinity-http-oss.png](gradual-scale-up-affinity-http-oss.png)

### Scale Down Gradually

#### Test: Send https /tea traffic

```text
Requests      [total, rate, throughput]         48000, 100.00, 100.00
Duration      [total, attack, wait]             8m0s, 8m0s, 1.151ms
Latencies     [min, mean, 50, 90, 95, 99, max]  651.444µs, 1.194ms, 1.181ms, 1.348ms, 1.417ms, 1.747ms, 31.936ms
Bytes In      [total, mean]                     7353552, 153.20
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:48000  
Error Set:
```

![gradual-scale-down-affinity-https-oss.png](gradual-scale-down-affinity-https-oss.png)

#### Test: Send http /coffee traffic

```text
Requests      [total, rate, throughput]         48000, 100.00, 100.00
Duration      [total, attack, wait]             8m0s, 8m0s, 1.543ms
Latencies     [min, mean, 50, 90, 95, 99, max]  625.439µs, 1.158ms, 1.149ms, 1.315ms, 1.378ms, 1.697ms, 29.523ms
Bytes In      [total, mean]                     7641540, 159.20
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:48000  
Error Set:
```

![gradual-scale-down-affinity-http-oss.png](gradual-scale-down-affinity-http-oss.png)

### Scale Up Abruptly

#### Test: Send https /tea traffic

```text
Requests      [total, rate, throughput]         12000, 100.01, 100.01
Duration      [total, attack, wait]             2m0s, 2m0s, 1.212ms
Latencies     [min, mean, 50, 90, 95, 99, max]  648.427µs, 1.189ms, 1.186ms, 1.343ms, 1.398ms, 1.591ms, 8.864ms
Bytes In      [total, mean]                     1838463, 153.21
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:12000  
Error Set:
```

![abrupt-scale-up-affinity-https-oss.png](abrupt-scale-up-affinity-https-oss.png)

#### Test: Send http /coffee traffic

```text
Requests      [total, rate, throughput]         12000, 100.01, 100.01
Duration      [total, attack, wait]             2m0s, 2m0s, 1.033ms
Latencies     [min, mean, 50, 90, 95, 99, max]  683.202µs, 1.25ms, 1.191ms, 1.375ms, 1.442ms, 1.687ms, 215.314ms
Bytes In      [total, mean]                     1910511, 159.21
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:12000  
Error Set:
```

![abrupt-scale-up-affinity-http-oss.png](abrupt-scale-up-affinity-http-oss.png)

### Scale Down Abruptly

#### Test: Send https /tea traffic

```text
Requests      [total, rate, throughput]         12000, 100.01, 100.01
Duration      [total, attack, wait]             2m0s, 2m0s, 1.186ms
Latencies     [min, mean, 50, 90, 95, 99, max]  685.26µs, 1.191ms, 1.188ms, 1.346ms, 1.409ms, 1.594ms, 12.06ms
Bytes In      [total, mean]                     1838451, 153.20
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:12000  
Error Set:
```

![abrupt-scale-down-affinity-https-oss.png](abrupt-scale-down-affinity-https-oss.png)

#### Test: Send http /coffee traffic

```text
Requests      [total, rate, throughput]         12000, 100.01, 100.01
Duration      [total, attack, wait]             2m0s, 2m0s, 823.136µs
Latencies     [min, mean, 50, 90, 95, 99, max]  646.596µs, 1.162ms, 1.166ms, 1.325ms, 1.381ms, 1.562ms, 12.055ms
Bytes In      [total, mean]                     1910395, 159.20
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:12000  
Error Set:
```

![abrupt-scale-down-affinity-http-oss.png](abrupt-scale-down-affinity-http-oss.png)

## Multiple NGINX Pods run per node Test Results

### Scale Up Gradually

#### Test: Send https /tea traffic

```text
Requests      [total, rate, throughput]         30000, 100.00, 100.00
Duration      [total, attack, wait]             5m0s, 5m0s, 1.174ms
Latencies     [min, mean, 50, 90, 95, 99, max]  639.841µs, 1.198ms, 1.182ms, 1.353ms, 1.43ms, 1.818ms, 24.143ms
Bytes In      [total, mean]                     4619796, 153.99
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      0:1  200:29999  
Error Set:
Get "https://cafe.example.com/tea": dial tcp 0.0.0.0:0->35.230.31.19:443: connect: connection refused
```

![gradual-scale-up-https-oss.png](gradual-scale-up-https-oss.png)

#### Test: Send http /coffee traffic

```text
Requests      [total, rate, throughput]         30000, 100.00, 100.00
Duration      [total, attack, wait]             5m0s, 5m0s, 977.684µs
Latencies     [min, mean, 50, 90, 95, 99, max]  632.63µs, 1.221ms, 1.168ms, 1.342ms, 1.418ms, 1.805ms, 215.589ms
Bytes In      [total, mean]                     4785071, 159.50
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```

![gradual-scale-up-http-oss.png](gradual-scale-up-http-oss.png)

### Scale Down Gradually

#### Test: Send http /coffee traffic

```text
Requests      [total, rate, throughput]         96000, 100.00, 100.00
Duration      [total, attack, wait]             16m0s, 16m0s, 1.227ms
Latencies     [min, mean, 50, 90, 95, 99, max]  586.914µs, 1.194ms, 1.18ms, 1.347ms, 1.417ms, 1.749ms, 217.951ms
Bytes In      [total, mean]                     15312219, 159.50
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:96000  
Error Set:
```

![gradual-scale-down-http-oss.png](gradual-scale-down-http-oss.png)

#### Test: Send https /tea traffic

```text
Requests      [total, rate, throughput]         96000, 100.00, 100.00
Duration      [total, attack, wait]             16m0s, 16m0s, 1.215ms
Latencies     [min, mean, 50, 90, 95, 99, max]  642.507µs, 1.213ms, 1.195ms, 1.368ms, 1.443ms, 1.778ms, 209.657ms
Bytes In      [total, mean]                     14783854, 154.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:96000  
Error Set:
```

![gradual-scale-down-https-oss.png](gradual-scale-down-https-oss.png)

### Scale Up Abruptly

#### Test: Send http /coffee traffic

```text
Requests      [total, rate, throughput]         12000, 100.01, 100.01
Duration      [total, attack, wait]             2m0s, 2m0s, 1.17ms
Latencies     [min, mean, 50, 90, 95, 99, max]  687.211µs, 1.228ms, 1.216ms, 1.398ms, 1.471ms, 1.799ms, 34.351ms
Bytes In      [total, mean]                     1913915, 159.49
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:12000  
Error Set:
```

![abrupt-scale-up-http-oss.png](abrupt-scale-up-http-oss.png)

#### Test: Send https /tea traffic

```text
Requests      [total, rate, throughput]         12000, 100.01, 100.01
Duration      [total, attack, wait]             2m0s, 2m0s, 1.111ms
Latencies     [min, mean, 50, 90, 95, 99, max]  732.378µs, 1.272ms, 1.251ms, 1.465ms, 1.547ms, 1.839ms, 21.969ms
Bytes In      [total, mean]                     1847974, 154.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:12000  
Error Set:
```

![abrupt-scale-up-https-oss.png](abrupt-scale-up-https-oss.png)

### Scale Down Abruptly

#### Test: Send http /coffee traffic

```text
Requests      [total, rate, throughput]         12000, 100.01, 100.01
Duration      [total, attack, wait]             2m0s, 2m0s, 1.305ms
Latencies     [min, mean, 50, 90, 95, 99, max]  690.951µs, 1.257ms, 1.238ms, 1.459ms, 1.559ms, 1.893ms, 13.163ms
Bytes In      [total, mean]                     1913879, 159.49
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:12000  
Error Set:
```

![abrupt-scale-down-http-oss.png](abrupt-scale-down-http-oss.png)

#### Test: Send https /tea traffic

```text
Requests      [total, rate, throughput]         12000, 100.01, 100.01
Duration      [total, attack, wait]             2m0s, 2m0s, 1.312ms
Latencies     [min, mean, 50, 90, 95, 99, max]  728.606µs, 1.306ms, 1.267ms, 1.498ms, 1.602ms, 1.983ms, 37.944ms
Bytes In      [total, mean]                     1847937, 153.99
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:12000  
Error Set:
```

![abrupt-scale-down-https-oss.png](abrupt-scale-down-https-oss.png)
