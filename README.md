# fail2ban-tightvncserver
To enable fail2ban for tightvncserver do the following:

1) Add tighvnc-auth.conf to /etc/fail2ban/filter.d

2) Add following to /etc/fail2ban/jail.conf

```
[tighvnc-auth]
enabled = true
port = 5901
filter = tighvnc-auth
logpath = <YOUR LOGPATH (example: /home/<user>/.vnc/*.log)>
bantime = 86400
findtime = 3600
maxretry = 3
```

3) Adjust logpath according to your tightvnc-installtion.
