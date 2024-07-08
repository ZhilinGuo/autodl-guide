# AutoDL guide

<!-- ## Brief Description -->
Tips and tools to use AutoDL for deep learning collaboration.

## Login

https://www.autodl.com

## Connect with VS Code
Convert ssh command to ssh config example:

```
ssh -p 12345 root@connect.cqa1.seetacloud.com

Host AutoDL
    HostName connect.cqa1.seetacloud.com
    User root
    Port 12345
```

<!-- haizhu -->
## Available drives
**General:** There are 3 disks in our virtual machine, namely system disk, data disk and AutoDL file storage. Data in all 3 of them will not be lost when the power is off.

| Name | Path | Size | Performance | Illustrate |
| ---- | ---- | ---- | ----------- | ---------- |
| system disk | /(root) | 30G | fast/local | The data will not be lost when the instance is shut down. Generally, system dependencies and Python installation packages will be installed on the system disk, and small-capacity data such as code can also be stored; when migrating an instance, it will be migrated, and when saving an image, it will be saved in the image. |
| data disk | /root/autodl-tmp | 50G(expandable) | fast/local | The data will not be lost when the instance is shut down. Data with high read and write IO requirements can be stored. However, it cannot be saved to the image or migrated. |
| AutoDL file storage | /root/autodl-fs | 20G for free | normal speed/network disk | It can realize file synchronization and sharing between different instances in the same region. |

<!-- haizhu -->
## Uploading and downloading dataset

## Bonus: Ping server regions
Chongqing-A
```
ping connect.cqa1.seetacloud.com
```

Beijing-A 
```
ping region-45.autodl.pro
```

Foshan 
```
ping region-9.autodl.pro
```
