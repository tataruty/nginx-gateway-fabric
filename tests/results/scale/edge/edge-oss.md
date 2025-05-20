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

## Test TestScale_Listeners

### Event Batch Processing

- Total: 325
- Average Time: 6ms
- Event Batch Processing distribution:
	- 500.0ms: 325
	- 1000.0ms: 325
	- 5000.0ms: 325
	- 10000.0ms: 325
	- 30000.0ms: 325
	- +Infms: 325

### Errors

- NGF errors: 13
- NGF container restarts: 0
- NGINX errors: 0
- NGINX container restarts: 0

### Graphs and Logs

See [output directory](./TestScale_Listeners) for more details.
The logs are attached only if there are errors.

## Test TestScale_HTTPSListeners

### Event Batch Processing

- Total: 392
- Average Time: 18ms
- Event Batch Processing distribution:
	- 500.0ms: 392
	- 1000.0ms: 392
	- 5000.0ms: 392
	- 10000.0ms: 392
	- 30000.0ms: 392
	- +Infms: 392

### Errors

- NGF errors: 18
- NGF container restarts: 0
- NGINX errors: 0
- NGINX container restarts: 0

### Graphs and Logs

See [output directory](./TestScale_HTTPSListeners) for more details.
The logs are attached only if there are errors.

## Test TestScale_HTTPRoutes

### Event Batch Processing

- Total: 1009
- Average Time: 92ms
- Event Batch Processing distribution:
	- 500.0ms: 1009
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

- Total: 157
- Average Time: 76ms
- Event Batch Processing distribution:
	- 500.0ms: 157
	- 1000.0ms: 157
	- 5000.0ms: 157
	- 10000.0ms: 157
	- 30000.0ms: 157
	- +Infms: 157

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
Requests      [total, rate, throughput]         30000, 1000.04, 1000.00
Duration      [total, attack, wait]             30s, 29.999s, 988.104µs
Latencies     [min, mean, 50, 90, 95, 99, max]  712.191µs, 939.08µs, 919.118µs, 1.034ms, 1.081ms, 1.213ms, 22.584ms
Bytes In      [total, mean]                     4770000, 159.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```
```text
Requests      [total, rate, throughput]         30000, 1000.04, 1000.00
Duration      [total, attack, wait]             30s, 29.999s, 987.954µs
Latencies     [min, mean, 50, 90, 95, 99, max]  819.222µs, 1.026ms, 1.008ms, 1.126ms, 1.178ms, 1.327ms, 10.006ms
Bytes In      [total, mean]                     4770000, 159.00
Bytes Out     [total, mean]                     0, 0.00
Success       [ratio]                           100.00%
Status Codes  [code:count]                      200:30000  
Error Set:
```
