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

## Test 1: Resources exist before startup - NumResources 30

### Time to Ready

Time To Ready Description: From when NGF starts to when the NGINX configuration is fully configured
- TimeToReadyTotal: 28s

### Event Batch Processing

- Event Batch Total: 8
- Event Batch Processing Average Time: 28ms
- Event Batch Processing distribution:
	- 500.0ms: 8
	- 1000.0ms: 8
	- 5000.0ms: 8
	- 10000.0ms: 8
	- 30000.0ms: 8
	- +Infms: 8

### NGINX Error Logs


## Test 1: Resources exist before startup - NumResources 150

### Time to Ready

Time To Ready Description: From when NGF starts to when the NGINX configuration is fully configured
- TimeToReadyTotal: 6s

### Event Batch Processing

- Event Batch Total: 9
- Event Batch Processing Average Time: 26ms
- Event Batch Processing distribution:
	- 500.0ms: 9
	- 1000.0ms: 9
	- 5000.0ms: 9
	- 10000.0ms: 9
	- 30000.0ms: 9
	- +Infms: 9

### NGINX Error Logs


## Test 2: Start NGF, deploy Gateway, wait until NGINX agent instance connects to NGF, create many resources attached to GW - NumResources 30

### Time to Ready

Time To Ready Description: From when NGINX receives the first configuration created by NGF to when the NGINX configuration is fully configured
- TimeToReadyTotal: 27s

### Event Batch Processing

- Event Batch Total: 227
- Event Batch Processing Average Time: 37ms
- Event Batch Processing distribution:
	- 500.0ms: 216
	- 1000.0ms: 227
	- 5000.0ms: 227
	- 10000.0ms: 227
	- 30000.0ms: 227
	- +Infms: 227

### NGINX Error Logs


## Test 2: Start NGF, deploy Gateway, wait until NGINX agent instance connects to NGF, create many resources attached to GW - NumResources 150

### Time to Ready

Time To Ready Description: From when NGINX receives the first configuration created by NGF to when the NGINX configuration is fully configured
- TimeToReadyTotal: 144s

### Event Batch Processing

- Event Batch Total: 1098
- Event Batch Processing Average Time: 44ms
- Event Batch Processing distribution:
	- 500.0ms: 1059
	- 1000.0ms: 1080
	- 5000.0ms: 1098
	- 10000.0ms: 1098
	- 30000.0ms: 1098
	- +Infms: 1098

### NGINX Error Logs

