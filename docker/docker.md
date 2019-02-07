# Docker Cheat Sheet
## Install
```
curl -sSL https://get.Docker.com/ | bash -x 
```

## Uninstall
```
sudo apt-get purge docker-engine
sudo apt-get autoremove --purge docker-engine
rm -rf /var/lib/docker
```

## Add User to Docker Group
```
sudo usermod -aG docker <user name>
```

## Add Mirror Registry
create or edit /etc/docker/daemon.json
```
{
  "registry-mirrors" : [
    "http://hub-mirror.c.163.com"
  ]
}
```