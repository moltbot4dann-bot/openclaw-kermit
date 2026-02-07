### Network

- LAN Interface: `enp0s31f6` (Primary preference)
- Wi-Fi Interface: `wlp2s0` (Backup only)
- Network Gateway: `192.168.2.1`
- Preferred State: Wi-Fi disabled, LAN cable preferred.

To force LAN and disable Wi-Fi:
`sudo ip route add default via 192.168.2.1 dev enp0s31f6 metric 100 && sleep 5 && sudo nmcli radio wifi off`
