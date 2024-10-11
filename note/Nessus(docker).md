# Nessus(docker)

```bash
# 拉取镜像
docker pull ramisec/nessus

docker run -itd --name=ramisec_nessus -p 28834:8834 ramisec/nessus
```

修改容器中的`nessus/update.sh`,将`update_url`修改为:

```bash
https://plugins.nessus.org/v2/nessus.php?f=all-2.0.tar.gz&u=56b33ade57c60a01058b1506999a2431&p=1ee9c89d5379a119a56498f2d5dff674
```

进入容器 bash 运行 update.sh 进行更新

```bash
./update.sh

# 更新编译完成后, 进入 /opt/nessus/sbin/ 修改 admin 密码(admin)
cd /opt/nessus/sbin/
./nessuscli chpasswd admin
```
