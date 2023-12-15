# LinuxCommands

Auto add ssh id to server
```
ssh-copy-id -i ~/.ssh/id_rsa.pub tom@SERVER_NAME
```

Find a process occupying a port
```
sudo lsof -i :PORT

COMMAND    PID USER   FD   TYPE  DEVICE SIZE/OFF NODE NAME
python  832673  tom    7u  IPv4 8794140      0t0  TCP *:zope-ftp (LISTEN)
python  832673  tom    8u  IPv4 8794141      0t0  TCP localhost:zope-ftp->localhost:36504 (CLOSE_WAIT)
```
Kill the process:
```
sudo kill -9 832673
```
