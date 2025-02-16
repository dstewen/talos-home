


### Talos Hosts 192.168.10.51 - 192.168.10.69

| Name | Device           | CPU       | OS Disk             | Data Disk          | RAM  | OS             | Purpose    | IP vPro (I226-LM) | IP Bond0 (2 x X710)                                                      | IP (1 x X710) |
| ---- | ---------------- | --------- | ------------------- | ------------------ | ---- | -------------- | ---------- | ----------------- | ------------------------------------------------------------------------ | ------------- |
| ms1 | Miniforums MS-01 | i9-13900H | Crucial CT500P1SSD8 | WD_BLACK SN770 2TB | 96GB | Talos (v1.9.3) | Controller | 192.168.30.50     | enp2s0f0np0 (58:47:ca:77:cf:36)<br>enp2s0f1np1<br>(58:47:ca:77:cf:37)    | 192.168.10.51 |
| ms2 | Miniforums MS-01 | i9-13900H | WD Blue SN570 500GB | WD_BLACK SN770 2TB | 96GB | Talos (v1.9.3) | Controller | 192.168.30.51     | enp2s0f0np0<br>(58:47:ca:78:f1:32)<br>enp2s0f1np1<br>(58:47:ca:78:f1:33) | 192.168.10.52 |
| ms3 | Miniforums MS-01 | i9-13900H | WD Blue SN570 500GB | WD_BLACK SN770 2TB | 96GB | Talos (v1.9.3) | Controller | 192.168.30.52     | enp2s0f0np0<br>(58:47:ca:78:f8:4a)<br>enp2s0f1np1<br>(58:47:ca:78:f8:4b) | 192.168.10.53 |

Total CPU: XX threads (workers)
Total RAM: XXXGB (workers)

### MS-01 Talos Cluster Ingresses

| Name                      | Purpose                                              | IP             |
| ------------------------- | ---------------------------------------------------- | -------------- |
| ingress_vip               | internal ingress load balancer                       | 192.168.10.26  |
| gateway_vip               | DNS to cluster                                       | 192.168.10.27  |
| tunnel_ingress_vip        | ingress for Cloudflare tunnels for external services | 192.168.10.28  |
| bootstrap_controllers_vip | IP address of the Kube API                           | 192.168.10.254 |



CM4 Workers

| Hostname | Model               | MAC               | Serial (EMMC) | Serial (NVME) | Role   | IP            | OS          | Firmware                                  | Status |
| -------- | ------------------- | ----------------- | ------------- | ------------- | ------ | ------------- | ----------- | ----------------------------------------- | ------ |
| blade4   | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.34 | Talos Linux | Sat 07 Dec 2024 12:39:28 UTC (1733575168) |        |
| blade5   | CM4 8Gb eMMC (32Gb) | e4:5f:01:ec:16:b4 | 8807de1e      |               | worker | 192.168.10.35 | Talos Linux | Sat 07 Dec 2024 12:39:28 UTC (1733575168) | Active |
| blade6   | CM4 8Gb eMMC (32Gb) | e4:5f:01:ec:16:a5 | f7b0297e      |               | worker | 192.168.10.36 | Talos Linux | Sat 07 Dec 2024 12:39:28 UTC (1733575168) | Active |
| blade7   | CM4 8Gb eMMC (32Gb) | e4:5f:01:ec:16:9c | 80ea8370      |               | worker | 192.168.10.37 | Talos Linux | Sat 07 Dec 2024 12:39:28 UTC (1733575168) |        |
| blade8   | CM4 8Gb eMMC (32Gb) | e4:5f:01:ec:16:5a | e2701412      |               | worker | 192.168.10.38 | Talos Linux | Sat 07 Dec 2024 12:39:28 UTC (1733575168) | Active |
| blade9   | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.39 | Talos Linux |                                           |        |
| blade10  | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.40 | Talos Linux |                                           |        |
| blade11  | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.41 | Talos Linux |                                           |        |
| blade12  | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.42 | Talos Linux |                                           |        |
| blade13  | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.43 | Talos Linux |                                           |        |
| blade14  | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.44 | Talos Linux |                                           |        |
| blade15  | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.45 | Talos Linux |                                           |        |
| blade16  | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.46 | Talos Linux |                                           |        |
| blade17  | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.47 | Talos Linux |                                           |        |
| blade18  | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.48 | Talos Linux |                                           |        |
| blade19  | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.49 | Talos Linux |                                           |        |
| blade20  | CM4 8Gb eMMC (32Gb) |                   |               |               | worker | 192.168.10.50 | Talos Linux |                                           |        |
| pi4cmio  | CM4 8Gb eMMC (32Gb) | e4:5f:01:50:27:2d | d03141        |               | worker | 192.168.10.25 | Talos Linux |                                           |        |
| hayellow | CM4 8Gb eMMC (32Gb) |                   |               |               | worker |               | Talos Linux |                                           |        |


### CM-Infra Cluster


| Hostname | Model               | MAC | Serial | Role       | IP            | OS     | Firmware |
| -------- | ------------------- | --- | ------ | ---------- | ------------- | ------ | -------- |
| blade1   | CM4 8Gb eMMC (32Gb) |     |        | controller | 192.168.10.31 | Debian |          |
| blade2   | CM4 8Gb eMMC (32Gb) |     |        | controller | 192.168.10.32 | Debian |          |
| blade3   | CM4 8Gb eMMC (32Gb) |     |        | controller | 192.168.10.33 | Debian |          |

### CM-Infra Cluster Ingresses

| Name                      | Purpose                                              | IP             |
| ------------------------- | ---------------------------------------------------- | -------------- |
| ingress_vip               | internal ingress load balancer                       | 192.168.10.249 |
| gateway_vip               | DNS to cluster                                       | 192.168.10.248  |
| tunnel_ingress_vip        | ingress for Cloudflare tunnels for external services | 192.168.10.247  |
| bootstrap_controllers_vip | IP address of the Kube API                           | 192.168.10.253 |




Pi4's

| Hostname | Model               | MAC               | Serial (EMMC) | Serial (NVME) | Role   | IP            | OS          |
| -------- | ------------------- | ----------------- | ------------- | ------------- | ------ | ------------- | ----------- |
| pi4w1    | CM4 8Gb eMMC (32Gb) | dc:a6:32:b0:f8:81 | 48b8f0c0      |               | worker |               |             |
| pi4w2    | CM4 8Gb eMMC (32Gb) |                   | 8807de1e      |               | worker |               |             |
| pi4w3    | CM4 8Gb eMMC (32Gb) |                   | f7b0297e      |               | worker |               |             |







### Supporting Hardware

| Name | Device | CPU | OS Disk | Data Disk | Cache Disk | RAM | OS | Purpose |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| NAS | Synology DS918+ | J3455 | - | 27.3TB | 2 x 500GB SSD | 8GB | DSM 7.2 | NAS/NFS/Backup |
| Pi3B | Raspberry Pi3B | Cortex A53 | 16GB mSD | - | - | 1GB | Raspbian/Nut |  |

### Networking/UPS Hardware

| Device          | Purpose                      |              |
| --------------- | ---------------------------- | ------------ |
| APC UPS         | UPS - Network                |              |
| SG1100          | Router                       | 192.168.10.1 |
| FS S3700-24T4F  | 24 Port Switch - Network     |              |
| FS S3400-48T6SP | 48 Port POE Switch - Network |              |
