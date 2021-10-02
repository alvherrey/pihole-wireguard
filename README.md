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

