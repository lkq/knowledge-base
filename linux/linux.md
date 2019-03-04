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

```
# Network Manager UI
nmtui
```
```
# join wifi
sudo sh -c "wpa_passphrase <WIFI Name> >> /etc/wpa_supplicant/wpa_supplicant.conf"
```

```
# restart network interface
ifdown wlan0
ifup wlan0
```

```
# edit sudo permission
sudo visudo
```

```
# systemd
systemctl daemon-reload
systemctl enable service-name
systemctl start service-name
```

```
# lis processes, order by memory usage
top -o %MEM
```

```
# install dnsutils - nslookup/dig (debian)
sudo apt-get install dnsutils
```
