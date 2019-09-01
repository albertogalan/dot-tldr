# ip

> Show / manipulate routing, devices, policy routing and tunnels.

- List interfaces with detailed info:

`ip a`

- Display the routing table:

`ip r`

- Make an interface up/down:

`ip link set {{interface}} up/down`

- Add/Delete an ip address to an interface:

`ip addr add/del {{ip}}/{{mask}} dev {{interface}}`

- Add a default route:

`ip route add default via {{ip}} dev {{interface}}`
- list all routes

`ip route list table all`


- up an interface

`ip link set dev eno1 up`


- Show gateway and routes

`ip route show`


