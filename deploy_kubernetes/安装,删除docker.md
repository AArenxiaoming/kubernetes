# 安装docker

# https://docs.docker.com/engine/install/centos/

```
sudo yum install -y yum-utils device-mapper-persistent-data lvm2
sudo yum-config-manager --add-repo http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo
yum -y install docker-ce
systemctl enable docker && systemctl start docker
# centos 8  https://www.cnblogs.com/zbseoag/p/11736006.html
# yum-config-manager  --add-repo   https://download.docker.com/linux/centos/docker-ce.repo
```

# 删除docker

sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine