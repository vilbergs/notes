# Docker

Printing out all network subnets being used by Docker
```bash
for network in $(docker network ls -q); do echo $network: $(docker network inspect $network | grep Subnet); done
```

