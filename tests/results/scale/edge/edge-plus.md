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

## Test TestScale_Listeners

### Event Batch Processing

- Total: 325
- Average Time: 128ms
- Event Batch Processing distribution:
	- 500.0ms: 283
	- 1000.0ms: 325
	- 5000.0ms: 325
	- 10000.0ms: 325
	- 30000.0ms: 325
	- +Infms: 325

### Errors

- NGF errors: 9
- NGF container restarts: 0
- NGINX errors: 178
- NGINX container restarts: 0

### Graphs and Logs

See [output directory](./TestScale_Listeners) for more details.
The logs are attached only if there are errors.

## Test TestScale_HTTPSListeners

### Event Batch Processing

- Total: 390
- Average Time: 120ms
- Event Batch Processing distribution:
	- 500.0ms: 345
	- 1000.0ms: 390
	- 5000.0ms: 390
	- 10000.0ms: 390
	- 30000.0ms: 390
	- +Infms: 390

### Errors

- NGF errors: 14
- NGF container restarts: 0
- NGINX errors: 171
- NGINX container restarts: 0

### Graphs and Logs

See [output directory](./TestScale_HTTPSListeners) for more details.
The logs are attached only if there are errors.

## Test TestScale_HTTPRoutes

### Event Batch Processing

- Total: 1009
- Average Time: 171ms
- Event Batch Processing distribution:
	- 500.0ms: 1008
	- 1000.0ms: 1009
	- 5000.0ms: 1009
	- 10000.0ms: 1009
	- 30000.0ms: 1009
	- +Infms: 1009

### Errors

- NGF errors: 0
- NGF container restarts: 0
- NGINX errors: 0
- NGINX container restarts: 0

### Graphs and Logs

See [output directory](./TestScale_HTTPRoutes) for more details.
The logs are attached only if there are errors.

## Test TestScale_UpstreamServers

### Event Batch Processing

- Total: 33
- Average Time: 511ms
- Event Batch Processing distribution:
	- 500.0ms: 19
	- 1000.0ms: 29
	- 5000.0ms: 33
	- 10000.0ms: 33
	- 30000.0ms: 33
	- +Infms: 33

### Errors

- NGF errors: 1
- NGF container restarts: 0
- NGINX errors: 0
- NGINX container restarts: 0

### Graphs and Logs

See [output directory](./TestScale_UpstreamServers) for more details.
The logs are attached only if there are errors.

## Test TestScale_HTTPMatches

```text
Requests      [total, rate, throughput]         29999, 1000.00, 999.98
Duration      [total, attack, wait]             30s, 29.999s, 800.545µs
Latencies     [min, mean, 50, 90, 95, 99, max]  691.408µs, 928.268µs, 907.578µs, 1.031ms, 1.076ms, 1.197ms, 15.712ms
Bytes In      [total, mean]                     4799840, 160.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:29999  
Error Set:
```
```text
Requests      [total, rate, throughput]         30000, 1000.02, 999.99
Duration      [total, attack, wait]             30s, 29.999s, 941.298µs
Latencies     [min, mean, 50, 90, 95, 99, max]  789.486µs, 1.009ms, 991.314µs, 1.118ms, 1.175ms, 1.301ms, 22.133ms
Bytes In      [total, mean]                     4800000, 160.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```
