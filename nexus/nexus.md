## Default Login
admin/admin123

## Run as Service
Set run as user in /bin/nexus.rc
```
run_as_user="<your user>"
```

create nexus.service under /etc/systemd/system/ with below content:
```
[Unit]
Description=Nexus Service
After=network.target
  
[Service]
Type=forking
LimitNOFILE=65536
ExecStart=<nexus install path>/bin/nexus start
ExecStop=<nexus install path>/bin/nexus stop
User=<your user>
Restart=on-abort
  
[Install]
WantedBy=multi-user.target
```

start service with systemctl
```
sudo systemctl daemon-reload
sudo systemctl enable nexus.service
sudo systemctl start nexus.service
```