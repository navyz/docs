## Install package

### CentOS/RHEL

```sh
sudo yum makecache
sudo yum install xxx
```

### Debian

```sh
sudo apt update
sudo apt install xxx
```

### Ubuntu

```sh
sudo apt update
sudo apt install xxx
```

### SLES

```sh
sudo zypper refresh
sudo zypper install
```

### Windows

```powershell
googet update
```



## List services

### CentOS/RHEL

```sh
sudo systemctl list-unit-files \
| grep google | grep enabled
```

### Debian

```sh
sudo systemctl list-unit-files \
| grep google | grep enabled
```

### Ubuntu

```sh
sudo systemctl list-unit-files \
| grep google | grep enabled
```

### Container-Optimized OS

```
sudo systemctl list-unit-files \
| grep google
```

### SLES

```sh
sudo systemctl list-unit-files \
| grep google | grep enabled
```

### Windows

```powershell
Get-Service GCEAgent
Get-ScheduledTask GCEStartup
```





## List installed packages

### CentOS/RHEL

```sh
rpm -qa --queryformat '%{NAME}\n' \
|grep -iE google\|gce | grep -iE \
'google|gce'
```

### Debian

```sh
apt list --installed \
| grep -iE 'google'
```

### Ubuntu

```sh
apt list --installed \
| grep -iE "google"
```

### Suse

```
rpm -qa --queryformat '%{NAME}\n' \
|grep -iE google
```

### Windows

```powershell
googet installed
```