# pihole-wireguard
Integrates Pihole with Wireguard

Requirements:
1. Configure duckdns dynamic dns -> see my duckdns repo (https://github.com/alvherrey/duckdns)
2. open udp port on the router firewall 51820 and map it to the wireguard server

Before start pihole container is needed to run the nexts commands on the host:
```
systemctl disable systemd-resolved.service
systemctl stop systemd-resolved
```

Obtain peer QR from wireguard container (number depends on number of peers availabes)
```
docker exec -it wireguard wg
docker exec -it wireguard /app/show-peer 1
```
Obtain peer config from wireguard container (number depends on number of peers availabes)
```
cat /opt/wireguard/config/peer1/peer1.conf
```
