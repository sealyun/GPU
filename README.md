# GPU
GPU docker runtime and device plugin

install.sh...

/etc/docker/daemon.json
```
[root@compute-gpu006 ~]# cat /etc/docker/daemon.json
{
    "default-runtime":"nvidia",
    "runtimes": {
        "nvidia": {
            "path": "/usr/bin/nvidia-container-runtime",
            "runtimeArgs": []
        }
    }
}
```

kubectl describe node xxx:
```
Capacity:
 cpu:                72
 ephemeral-storage:  222779Mi
 hugepages-1Gi:      0
 hugepages-2Mi:      2Gi
 memory:             791014684Ki
 nvidia.com/gpu:     2
 pods:               110
Allocatable:
 cpu:                72
 ephemeral-storage:  210240641086
 hugepages-1Gi:      0
 hugepages-2Mi:      2Gi
 memory:             788815132Ki
 nvidia.com/gpu:     2
 pods:               110
```
