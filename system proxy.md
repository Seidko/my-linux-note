## 使用 clash 配置系统代理
1. 安装 clash
```sh
pacman -S clash
```
2. 找一个位置放下配置文件
`download_config.sh`
```sh
cd "/clash/working/directory"
curl -o config.yaml YOUR_URL
chmod 666 config.yaml
```
3. 编写 clash daemon unit
```ini
[Unit]
Description=Clash Daemon
After=network-online.target

[Service]
User=clash
ExecStart=/bin/clash
Restart=on-failure
WorkingDirectory="/clash/working/directory"

[Install]
WantedBy=multi-user.target
```
4. 启动 unit
```sh
systemctl daemon-reload
systemctl enable clash --now
```
5. 在系统代理中加入对应服务器
    - KDE：网络设置 -> 代理 -> 使用系统代理服务器配置 -> 配置 http 和 socks 代理
