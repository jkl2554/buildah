# Install Buildah

## Install buildah CentOS & Redhat  
```
sudo yum update
sudo yum install buildah 
```
### Rootless buildah
Centos 및 redhat에서 rootless buildah 실행 시
```
kernel does not support overlay fs: 'overlay' is not supported over <unknown> at "/home/<username>/.local/share/containers/storage/overlay": backing file system is unsupported for this graph driver
WARN[0000] failed to shutdown storage: "kernel does not support overlay fs: 'overlay' is not supported over xfs at \"/home/<username>/.local/share/containers/storage/overlay\": backing file system is unsupported for this graph driver"
ERRO[0000] exit status 125
```
오류 발생할 경우
```
yum install fuse-overlayfs
```
설치 후 실행하면 정상적으로 작동