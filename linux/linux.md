## Setup Command Alias
```
echo "alias ll='ls -alG'" >> ~/.bash_aliases
```

## Change Open File Limit
```
vi /etc/security/limits.conf
#* hard nofile xxx
#* soft nofile xxx
```

## Config Static IP Address
```
vi /etc/dhcpcd.conf

# append
interface wlan0
static ip_address=192.168.1.252
static routers=192.168.1.1
static domain_name_servers=192.168.1.1 8.8.8.8
# reboot
```

## Useful Commands
edit sudo
```
sudo visudo
```

systemd

systemctl daemon-reload
systemctl enable service-name
systemctl start service-name