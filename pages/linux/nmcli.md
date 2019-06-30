# nmcli

> A command line tool for controlling NetworkManager.

- List all NetworkManager connections (shows name, uuid, type and device):

`nmcli connection`

- Activate a connection by specifying an uuid:

`nmcli connection up uuid {{uuid}}`

- Deactivate a connection:

`nmcli connection down uuid {{uuid}}`

- Print statuses of network interfaces:

`nmcli device status`


- Connect to a network

`nmcli device wifi rescan;nmcli device wifi list;nmcli device wifi connect 'Agora Space' password 'getstuffdone'`

- Activate hotstop

`nmcli device wifi hotspot ifname wlx00c0ca663eb3 con-name {{conname}} ssid agalan; password {{password}};nmcli connection show; nmcli  con up  {{conname}}`

- Delete a wifi connection

`nmcli con delete Wifi`

- Edit

`nmcli con edit xxxx;print`

- examples

`https://developer.gnome.org/NetworkManager/stable/nmcli.html`
`https://people.freedesktop.org/~lkundrak/nm-docs/nmcli-examples.html`
- Show dns server IP

`nmcli device show wlp1s0`


- Remove waiting network on boot

`systemctl mask systemd-networkd-wait-online.service`


