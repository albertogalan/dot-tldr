# telnet

> Connect to a specified port of a host using the telnet protocol.

- Telnet to the default port of a host:

`telnet {{host}}`

- Telnet to a specific port of a host:

`telnet {{ip_address}} {{port}}`

- Exit a telnet session:

`quit`

- Emit the default escape character combination for terminating the session:

`Ctrl + ]`

- Start telnet with "x" as the session termination character:

`telnet -e {{x}} {{ip_address}} {{port}}`

- More about telnet
`https://www.ict.tuwien.ac.at/lva/384.081/datacom/A2-Standard_Applications_v6-0.pdf`
