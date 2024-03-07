## Tested Environment
- Ubuntu 22.04
- AWS Lightsail

## Prerequisites
- Any OS (tested on Ubuntu 22.04 only)
Docker and Docker Compose is required
- Installed:
  - [Docker](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-22-04)
  - [Docker Compose](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-22-04)
- 51820/UDP port should be open in public. Recommend to search with keyword `Port forwarding`.

## Getting Started

1. Meet all the requirements from `Prerequisites` section.

2. Run docker container:
```
git clone https://github.com/lentil32/wireguard-with-adguard
cd wireguard-with-adguard
sudo docker compose up -d
```

3. Go to folder and copy the content of config file (e.g. `peer1.conf`):
```
cd wireguard/peer1
cat peer1.conf
```

4. Put the content from `3` into your WireGuard VPN tunnel configuration.

5. Connect to the instance.

6. Go to `http://10.2.0.100:3000` and complete the initilization.
- Without this step, clients cannot get DNS records so they can only
  connect to internet with IP e.g., `1.1.1.1`.
