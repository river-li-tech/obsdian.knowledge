# 自部署 VPN 指南

## 1. VPS 服务商选择

### 1.1 推荐方案

- **DigitalOcean**  
  官网：[https://www.digitalocean.com/](https://www.digitalocean.com/)  
  备注：服务器密码 RiverLi@1024bj

### 1.2 不可用方案

- **Vultr**  
  官网：[https://www.vultr.com/zh/?lang=zh](https://www.vultr.com/zh/?lang=zh)  
  备注：当前测试不可用，仅保留记录

### 1.3 备选方案

- **阿里云 ECS（香港节点）**  
  官网：[https://www.aliyun.com/product/ecs?spm=5176.19720258.J_8058803260.32.c9a82c4aHOBkyK](https://www.aliyun.com/product/ecs?spm=5176.19720258.J_8058803260.32.c9a82c4aHOBkyK)

- **Microsoft Azure**  
  官网：[https://azure.microsoft.com/zh-cn/](https://azure.microsoft.com/zh-cn/)

---

## 2. 部署方法

### 2.1 教程资源

- 视频教程：  
  [https://www.youtube.com/watch?v=RrBYepAcxrk](https://www.youtube.com/watch?v=RrBYepAcxrk)

- sing-box 一键安装脚本：  
  [https://github.com/233boy/sing-box](https://github.com/233boy/sing-box)

- Fork 后的安装脚本：  
  [https://github.com/river-li-tech/vpn-sing-box](https://github.com/river-li-tech/vpn-sing-box)

### 2.2 执行流程

#### 官方安装脚本

```bash
bash <(wget -qO- -o- https://github.com/233boy/sing-box/raw/main/install.sh)
```

#### Fork 后的安装脚本

```bash
bash <(wget -qO- -o- https://github.com/river-li-tech/vpn-sing-box/blob/main/install.sh)
```

---

## 3. 客户端连接

- **V2RayN**：  
  [https://github.com/2dust/v2rayN/releases?page=1](https://github.com/2dust/v2rayN/releases?page=1)

---

## 4. 常见问题

### 4.1 SSH Key 冲突

如果服务器重建或更换 IP 后出现 SSH key 冲突，可执行以下命令删除本地旧记录：

```bash
ssh-keygen -R <server-ip>
```

### 4.2 Mac 下设置应用权限

#### 查看隔离属性

```bash
xattr "/Applications/v2rayN.app"
```

#### 移除隔离属性

```bash
sudo xattr -rd com.apple.quarantine "/Applications/v2rayN.app"
```

---

## 5. 域名注册与加速

- **域名注册**：  
  [https://www.namesilo.com/account_domains.php](https://www.namesilo.com/account_domains.php)

- **域名加速 / 映射（Cloudflare）**：  
  [https://dash.cloudflare.com/](https://dash.cloudflare.com/)

