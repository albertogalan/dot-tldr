# arp-scan

> Send ARP packets to hosts (specified as IP addresses or hostnames) to scan the local network.

- Scan the current local network:

`arp-scan --localnet`

- Scan an IP network with a custom bitmask:

`arp-scan {{192.168.1.1}}/{{24}}`

- Scan an IP network within a custom range:

`arp-scan {{127.0.0.0}}-{{127.0.0.31}}`

- Scan an IP network with a custom net mask:

`arp-scan {{10.0.0.0}}:{{255.255.255.0}}`
- scan ip and mac address / if want vendor name also with get-oui
`get-oui`
`arp-scan -l`


