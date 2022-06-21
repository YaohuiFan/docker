# Docker Networking

**Dockering networking** is primarily used for communication established between Docker containers and the outside world through the host machine where the Docker daemon is operating. 

## Docker Network Drivers

Docker's networking subsystem is pluggable, using **drivers**. 

The following drivers are supported in Docker:

- [**bridge**](https://docs.docker.com/network/bridge/): the default network driver
- [**host**](https://docs.docker.com/network/host/): using the host's networking directly
- [**overlay**](https://docs.docker.com/network/overlay/): communication among multiple Docker daemons
- [**ipvlan**](): network based on IPv4 and IPv6 addressing
- [**macvlan**](https://docs.docker.com/network/macvlan/): assign a MAC address to each container, i.e. as a physical device on the Docker network
- [**none**](): distalbe the container networking
 

### [Networking with standalone containers](https://docs.docker.com/network/network-tutorial-standalone/)

- Use the default **bridge** network
- Use **user-defined** bridge network
- [Use **macvlan** network](https://docs.docker.com/network/network-tutorial-macvlan/)

#### Use macvlan network

The **macvlan** driver is only working on Linux hosts. It creates a macvlan network in two modes:
- bridge mode: triffic goes through a physical device on the host (usually the host's ethernet interface)
- 802.1q trunk bridge mode: traffic goes through an 802.1q sub-interface which Docker creates on the fly. Easy to control the routing and filtering

### [Networking with swamp services](https://docs.docker.com/network/network-tutorial-overlay/)
