# Linux Cheat Sheet

## Setup Alias
```
echo "alias ll='ls -alG'" >> ~/.bash_aliases
```

## Change Open File Limit
```
vi /etc/security/limits.conf
#* hard nofile xxx
#* soft nofile xxx
```