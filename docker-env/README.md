# Preparations
1. Install Multipass
   * We use Multipass to provide a consistent, lightweight Ubuntu virtual machine environment across different host operating systems. This ensures that all students work within the same Linux configuration, avoiding discrepancies caused by OS-specific Docker behavior or dependencies. It also isolates the exercise environment from the host, reducing the risk of conflicts or system misconfiguration.
   *  [Install Multipass](https://canonical.com/multipass/install)
2. Create a Multipass VM (Ubuntu Noble 24.04 (LTS))
```bash
multipass launch noble --name docker-vm --cpus 2 --mem 4G --disk 50G
```
3. Install Docker on a Multipass VM
   1. [Uninstall old versions](https://docs.docker.com/engine/install/ubuntu/#uninstall-old-versions)
   2. [Install using the apt repository](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)


# Useful Commands
```bash
# create instances specified in docker-compose.yml and run them in background
docker compose up -d 
```
```bash
# take down all created by the corresponding up
docker compose down
```
```bash
# list all containers
docker ps
```
```bash
# list all networks
docker network ls
```
```bash
# get an interactive shell of node1
docker exec node1 -it sh
```
```bash
# show network info
ip address
```

# Demo 1
- See [demo1/docker-compose.yml](../demo1/docker-compose.yml)
- Create three Linux instances ```node1,node2,node3```
- Create a network ```testnet```
- Check IP addresses of all nodes
- Send ping to each other