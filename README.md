# docker-debian-10 🐳
Debian 10 Docker install guide.
Perform the steps one after the other

----

Update apt-get
```
apt-get update
```

Installing prerequisite packages
```
apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```

Adding GPG key
```
curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
```

Adding fingerprint
```
apt-key fingerprint 0EBFCD88
```

Adding docker repository to apt
```
add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/debian \
   $(lsb_release -cs) \
   stable"
```

Updating apt
```
apt update
```

Changing apt cache
```
apt-cache policy docker-ce
```

Installing docker-ce
```
apt install docker-ce
```

Check
```
systemctl status docker
```
----
