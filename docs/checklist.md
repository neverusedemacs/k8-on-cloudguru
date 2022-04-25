# Checklist

### Kubernetes Host Requirements

This will run on just about any Linux OS, if you aren't following the guide then it would require some initial research to get all the right components installed.

### Full network connectivity

Lets go ahead and make this easier on ourselves to search for each node, we will configure DNS locally, in a production environment you won't have to do this.

We will go with this naming of the servers 

```text
control-plane
worker-1
worker-2
```
Log in to each server and run the below commands

```bash
nano /etc/hostname

change the hostname to one of the 3 above (each server should have a different hostname)
```

Reboot the server once you change the hostname for it to stick

Edit the hosts file on all the servers. They should all have the a line that maps IP to host names

They should look similar to the below (change to the right IP's)

```text
127.0.0.1 localhost
# The following lines are desirable for IPv6 capable hosts
::1 ip6-localhost ip6-loopback
# Cloud Server Hostname mapping
172.31.0.1   control-plane
172.31.0.2   worker-1
172.31.0.3    worker-2
```
### Unique Mac Address and UUID

Run the below commands to verify a different mac address and uuid

```bash
sudo cat /sys/class/dmi/id/product_uuid
ip link
```

