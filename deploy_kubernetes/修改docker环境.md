# 修改docker环境

```
 tee /etc/docker/daemon.json <<-'EOF'
{
  "registry-mirrors": ["https://bvae0o1g.mirror.aliyuncs.com"],
  "exec-opts": ["native.cgroupdriver=systemd"],
  "log-driver": "json-file",
  "log-opts": {
    "max-size": "100m"
  },
  "storage-driver": "overlay2",
  "storage-opts": [
    "overlay2.override_kernel_check=true"
  ]
}
EOF
```