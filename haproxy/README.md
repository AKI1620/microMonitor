# How To Install Haproxy in Ubuntu and Load the Mentioned Configuration

```
apt update
apt-get update
apt install haproxy
```

Ensure you fire and check the below commands that installed haproxy is running

```
systemctl start haproxy
systemctl enable haproxy
systemctl status haproxy
```

Now goto /etc/haproxy there will be one file named haproxy.cfg take a backup of it and replace it with the given file

> Note: To Change the minikube IP Present

Once Changes are Made ensure to restart haproxy.service

```
systemctl restart haproxy
systemctl status haproxy
```
