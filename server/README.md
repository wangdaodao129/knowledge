# 服务器相关

## 配置root用户密码
```bash
sudo passwd root
```

## 开启ssh
1. 安装SSH服务（如果尚未安装）
```bash
sudo apt-get update
sudo apt-get install openssh-server
```
2. 启动ssh服务
```bash
sudo systemctl start ssh 
```
3. 使SSH服务在系统启动时自动运行：
```bash
sudo systemctl enable ssh
```
4. 检查SSH服务状态
```bash
sudo systemctl status ssh
```

## 配置IP
### a.图形界面配置
打开网络设置(右上角的位置) ，点击“IPv4”，选择“Manual”（手动配置），分别输入IP地址Address、子网掩码Netmask、网关Gateway，以及DNS的可选，设置好了，点击右上角的 Apply（应用），如下图：

![图形IP配置](./images/ip.png)

### b.配置文件
进入配置文件
```bash
cd /etc/netplan

sudo vim 01-network-manager-all.yaml
```
按照如下配置

![IP配置文件](./images/ip_conf.png)
