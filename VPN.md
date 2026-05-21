
# 自部署VPN
- **VPS****服务商**（一般最便宜的5刀/月）
    
    - 【已选】DigtalOcean（GitHub教育优惠50$）：https://www.digitalocean.com/
        
    - 【不可用】Vultr [SSD VPS 服务器、云服务器和 Vultr 的云托管](https://www.vultr.com/zh/?lang=zh)
        
    - 阿里云（香港节点）[云服务器ECS_云主机_服务器托管_弹性计算-阿里云](https://www.aliyun.com/product/ecs?spm=5176.19720258.J_8058803260.32.c9a82c4aHOBkyK)
        
    - 微软Azurehttps://azure.microsoft.com/zh-cn/
        
- **搭建方法**
    
    - 购买物理机(google账号登录）
        
    - ~~Vultr：~~~~无法连接~~
        
        - ~~https://console.vultr.com/~~
            
        - ~~物理机密码：~~
            
    - DigtalOcean
        
        - https://cloud.digitalocean.com/droplets/571440350?i=2cb977
            
        - 物理机密码：RiverLi@1024bj
            
    - 搭建方法
        
        - 教程
            
            - 视频教程：https://www.youtube.com/watch?v=RrBYepAcxrk
                
            - singbox一键安装脚本github:https://github.com/233boy/sing-box
                
        - 执行流程
            
            ```JSON
            // 教程：安装脚本
            bash <(wget -qO- -o- https://github.com/233boy/sing-box/raw/main/install.sh)
            
            // Fork后的安装脚本
            bash <(wget -qO- -o- https://github.com/river-li-tech/vpn-sing-box/blob/main/install.sh)
            ```
            
- **连接方法**
    
    - V2RayN
        
        - V2RayN：https://github.com/2dust/v2rayN/releases?page=1
            
        - Mac下设置权限
            
        
        ```JSON
        // 查看隔离属性
        xattr "/Applications/v2rayN.app"
        // 移除隔离属性
        sudo xattr -rd com.apple.quarantine "/Applications/v2rayN.app"
        ```
        
- **其他问题**
    
    - sshkey冲突：删除本地ssh key
        
    
    ```JSON
    ssh-keygen -R 104.236.254.12
    ```



## 域名
域名注册：[[https://www.namesilo.com/account_domains.php]]
域名加速（映射）：[[https://dash.cloudflare.com/42d47157f02a4e4f1959c3d4f6e0f976/riverli.biz]]

