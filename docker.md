# Docker

## Useful commands

Printing out all network subnets being used by Docker
```bash
for network in $(docker network ls -q); do echo $network: $(docker network inspect $network | grep Subnet); done
```

## Configuring Docker daemon

The Mac and Windows Docker client will provide an interface to configure the daemon.json
You can edit (or create) the daemon configuration file in `/etc/docker/daemon.json`

### Overwriting the default bridge network subnet 

```javascript
{
  "bip": "172.26.0.1/16" // or any subnet of your choice
}
```
