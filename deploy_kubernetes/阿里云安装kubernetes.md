# 安装kubernetes 阿里云源

```
cat > /etc/yum.repos.d/kubernetes.repo << EOF
[kubernetes]
name=Kubernetes
baseurl=https://mirrors.aliyun.com/kubernetes/yum/repos/kubernetes-el7-x86_64
enabled=1
gpgcheck=0
repo_gpgcheck=0
gpgkey=https://mirrors.aliyun.com/kubernetes/yum/doc/yum-key.gpg https://mirrors.aliyun.com/kubernetes/yum/doc/rpm-package-key.gpg
EOF
```

```
yum install -y kubelet kubeadm kubectl
systemctl enable kubelet && systemctl start kubelet

```

# 指定版本
```
yum install -y kubelet-1.18.0 kubeadm-1.18.0 kubectl-1.18.0
```