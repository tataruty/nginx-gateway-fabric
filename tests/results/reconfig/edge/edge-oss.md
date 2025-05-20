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

## Test 1: Resources exist before startup - NumResources 30

### Time to Ready

Time To Ready Description: From when NGF starts to when the NGINX configuration is fully configured
- TimeToReadyTotal: 9s

### Event Batch Processing

- Event Batch Total: 10
- Event Batch Processing Average Time: 4ms
- Event Batch Processing distribution:
	- 500.0ms: 10
	- 1000.0ms: 10
	- 5000.0ms: 10
	- 10000.0ms: 10
	- 30000.0ms: 10
	- +Infms: 10

### NGINX Error Logs


## Test 1: Resources exist before startup - NumResources 150

### Time to Ready

Time To Ready Description: From when NGF starts to when the NGINX configuration is fully configured
- TimeToReadyTotal: 6s

### Event Batch Processing

- Event Batch Total: 10
- Event Batch Processing Average Time: 6ms
- Event Batch Processing distribution:
	- 500.0ms: 10
	- 1000.0ms: 10
	- 5000.0ms: 10
	- 10000.0ms: 10
	- 30000.0ms: 10
	- +Infms: 10

### NGINX Error Logs


## Test 2: Start NGF, deploy Gateway, wait until NGINX agent instance connects to NGF, create many resources attached to GW - NumResources 30

### Time to Ready

Time To Ready Description: From when NGINX receives the first configuration created by NGF to when the NGINX configuration is fully configured
- TimeToReadyTotal: 23s

### Event Batch Processing

- Event Batch Total: 296
- Event Batch Processing Average Time: 19ms
- Event Batch Processing distribution:
	- 500.0ms: 296
	- 1000.0ms: 296
	- 5000.0ms: 296
	- 10000.0ms: 296
	- 30000.0ms: 296
	- +Infms: 296

### NGINX Error Logs
2025/05/20 19:36:40 [emerg] 8#8: pread() returned only 0 bytes instead of 4085 in /etc/nginx/conf.d/http.conf:1160
2025/05/20 19:36:42 [emerg] 8#8: unexpected end of file, expecting "}" in /etc/nginx/conf.d/http.conf:2955
2025/05/20 19:36:43 [emerg] 8#8: unknown directive "roxy_set_header" in /etc/nginx/conf.d/http.conf:1081


## Test 2: Start NGF, deploy Gateway, wait until NGINX agent instance connects to NGF, create many resources attached to GW - NumResources 150

### Time to Ready

Time To Ready Description: From when NGINX receives the first configuration created by NGF to when the NGINX configuration is fully configured
- TimeToReadyTotal: 122s

### Event Batch Processing

- Event Batch Total: 1405
- Event Batch Processing Average Time: 28ms
- Event Batch Processing distribution:
	- 500.0ms: 1405
	- 1000.0ms: 1405
	- 5000.0ms: 1405
	- 10000.0ms: 1405
	- 30000.0ms: 1405
	- +Infms: 1405

### NGINX Error Logs
2025/05/20 19:47:56 [emerg] 8#8: unexpected end of file, expecting ";" or "}" in /etc/nginx/conf.d/http.conf:1608
2025/05/20 19:47:58 [emerg] 8#8: unexpected end of file, expecting "}" in /etc/nginx/conf.d/http.conf:2628
2025/05/20 19:47:59 [emerg] 8#8: pread() returned only 0 bytes instead of 4093 in /etc/nginx/conf.d/http.conf:1309
2025/05/20 19:47:59 [emerg] 8#8: pread() returned only 0 bytes instead of 2351 in /etc/nginx/conf.d/http.conf:2799
2025/05/20 19:48:02 [emerg] 8#8: unexpected end of file, expecting ";" or "}" in /etc/nginx/conf.d/http.conf:3947
2025/05/20 19:48:03 [emerg] 8#8: pread() returned only 0 bytes instead of 4095 in /etc/nginx/conf.d/http.conf:766
2025/05/20 19:48:04 [emerg] 8#8: unexpected end of file, expecting ";" or "}" in /etc/nginx/conf.d/http.conf:4492
2025/05/20 19:48:07 [emerg] 8#8: pread() returned only 0 bytes instead of 4091 in /etc/nginx/conf.d/http.conf:2140
2025/05/20 19:48:08 [emerg] 8#8: pread() returned only 0 bytes instead of 4086 in /etc/nginx/conf.d/http.conf:2509
2025/05/20 19:48:10 [emerg] 8#8: unexpected end of file, expecting ";" or "}" in /etc/nginx/conf.d/http.conf:6672
2025/05/20 19:48:12 [emerg] 8#8: pread() returned only 0 bytes instead of 4092 in /etc/nginx/conf.d/http.conf:1961
2025/05/20 19:48:12 [emerg] 8#8: pread() returned only 0 bytes instead of 4093 in /etc/nginx/conf.d/http.conf:6461
2025/05/20 19:48:16 [emerg] 8#8: unexpected end of file, expecting ";" or "}" in /etc/nginx/conf.d/http.conf:8961
2025/05/20 19:48:17 [emerg] 8#8: unexpected end of file, expecting ";" or "}" in /etc/nginx/conf.d/http.conf:9192
2025/05/20 19:48:19 [emerg] 8#8: pread() returned only 0 bytes instead of 4095 in /etc/nginx/conf.d/http.conf:3363
2025/05/20 19:48:20 [emerg] 8#8: pread() returned only 0 bytes instead of 4095 in /etc/nginx/conf.d/http.conf:4683
2025/05/20 19:48:22 [emerg] 8#8: unexpected end of file, expecting ";" or "}" in /etc/nginx/conf.d/http.conf:11044
2025/05/20 19:48:23 [emerg] 8#8: pread() returned only 0 bytes instead of 4089 in /etc/nginx/conf.d/http.conf:1517
2025/05/20 19:48:23 [emerg] 8#8: pread() returned only 0 bytes instead of 4083 in /etc/nginx/conf.d/http.conf:4254
2025/05/20 19:48:25 [emerg] 8#8: pread() returned only 0 bytes instead of 4095 in /etc/nginx/conf.d/http.conf:412
2025/05/20 19:48:25 [emerg] 8#8: unexpected end of file, expecting "}" in /etc/nginx/conf.d/http.conf:12547
2025/05/20 19:48:26 [emerg] 8#8: unexpected end of file, expecting ";" or "}" in /etc/nginx/conf.d/http.conf:12726
2025/05/20 19:48:27 [emerg] 8#8: unexpected end of file, expecting ";" or "}" in /etc/nginx/conf.d/http.conf:13162
2025/05/20 19:48:29 [emerg] 8#8: unexpected end of file, expecting "}" in /etc/nginx/conf.d/http.conf:13746
2025/05/20 19:48:29 [emerg] 8#8: pread() returned only 0 bytes instead of 4089 in /etc/nginx/conf.d/http.conf:5285
2025/05/20 19:48:32 [emerg] 8#8: pread() returned only 0 bytes instead of 4088 in /etc/nginx/conf.d/http.conf:3293
2025/05/20 19:48:34 [emerg] 8#8: pread() returned only 0 bytes instead of 4085 in /etc/nginx/conf.d/http.conf:1285
2025/05/20 19:48:35 [emerg] 8#8: unexpected end of file, expecting ";" or "}" in /etc/nginx/conf.d/http.conf:16046

