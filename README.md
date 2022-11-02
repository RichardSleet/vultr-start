# Vultr Script Startup
## Steps
1. Execute install v2ray script

```sh
bash <(curl -L https://raw.githubusercontent.com/v2fly/fhs-install-v2ray/master/install-release.sh) --version v4.44.0
```
2. Change v2ray config.json
```sh
vi /usr/local/etc/v2ray/config.json
```
3. MD5
```sh
vi /etc/systemd/system/v2ray.service

[Service]
Environment="V2RAY_VMESS_AEAD_FORCED=false"
```

4. Close firewall of debian
```sh
ufw disable
```

5. Change Time
```sh
timedatectl set-timezone Asia/Shanghai
```

6. Reboot
```sh
reboot
```

7. Start v2ray
`systemctl start v2ray`

8. CloudFare must use 80
