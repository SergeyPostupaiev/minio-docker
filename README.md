To launch minio in distributed mode you have to pass the location of all storage disks to the `command` in compose file, disks can be located on different servers: 
```
command: server http://<host_name>{1...n}/<disk_name/volume_name>{1...m}
```
Then run `docker-compose build && docker-compose up -d` on each server to launch distributed s3-compatible storage