# Jenkins Cheat Sheet

## Default Admin Password
```
cat ~/.jenkins/secrets/initialAdminPassword
```

## Run as Service

create jenkins.service under /etc/systemd/system/ with below content:
```
[Unit]
Description=Jenkins
After=network.target

[Service]
LimitNOFILE=65536
ExecStart=java -jar /home/<user name>/jenkins.war
User=<user name>

[Install]
WantedBy=multi-user.target

```

start service with systemctl
```
sudo systemctl daemon-reload
sudo systemctl enable jenkins.service
sudo systemctl start jenkins.service
```