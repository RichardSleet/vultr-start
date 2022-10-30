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
```
ufw disable
```

5. Reboot
```
reboot
```

6. Start v2ray
`systemctl start v2ray`

