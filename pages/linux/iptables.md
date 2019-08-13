# iptables

> Program that allows configuration of tables, chains and rules provided by the Linux kernel firewall.

- See chains and rules for specific table:

`sudo iptables -t {{table_name}} -vnL`

- Set chain policy rule:

`sudo iptables -P {{chain}} {{rule}}`

- Append rule to chain policy for IP:

`sudo iptables -A {{chain}} -s {{ip}} -j {{rule}}`

- Append rule to chain policy for IP considering protocol and port:

`sudo iptables -A {{chain}} -s {{ip}} -p {{protocol}} --dport {{port}} -j {{rule}}`

- Delete chain rule:

`sudo iptables -D {{chain}} {{rule_line_number}}`

- Save iptables configuration:

`sudo iptables-save > {{path/to/iptables_file}}`

- IP tables Flush

`sudo iptables -F`

- Save ip tables

`iptables-save > /etc/network/iptables.rules`

- Port redirection
`sysctl net.ipv4.ip_forward=1`
`iptables -t nat -A PREROUTING -p tcp -d MACHINE_B --dport 443 -j DNAT --to-destination MACHINE_C`
`iptables -t nat -A POSTROUTING -s MACHINE_A -o INTERFACE_NAME -j MASQUERADE`
