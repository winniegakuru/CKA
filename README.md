# CKA

### ETCD
- it is a distributed reliable key- value store that is simple, secure and fast.
 ##### Exampple
 ```
    {
      "Name":"Winnie Gakuru",
      "Gender":"Female",
      "Occupation":" DevOps"
    }
 ```
 #### Install ETCD
 1. Download Binaries
 ```
 wget -q --https-only \
"https://github.com/coreos/etcd/releases/download/v3.3.9/etcd-v3.3.9-linux-amd64.tar.gz"
 ```
 
 2. Extract 
 ```
  tar xzvf etcd-v3.3.9-linux-amd64.tar.gz
 ```
 
 3. Run ETCD service
 `./etcd`
 
###### Use `etcdctl` to run ETCD commands
```
./etcdctl set key1 value1
./etcdctl set key1 value1
./etcdctl
```
