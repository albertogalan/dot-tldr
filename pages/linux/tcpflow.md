# tcpflow

> Capture TCP traffic for debugging and analysis.

- Show all data on the given interface and port:

`tcpflow -c -i {{eth0}} port {{80}}`
- inspect tcp flow over a interface

`tcpflow -p -c -i eth0 port 80 | grep -oE '(GET|POST|HEAD) .* HTTP/1.[01]|Host: .*'`


