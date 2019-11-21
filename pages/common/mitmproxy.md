# mitmproxy

> An interactive man-in-the-middle HTTP proxy.

- Start mitmproxy with default settings:

`mitmproxy`

- Start mitmproxy bound to custom address and port:

`mitmproxy -b {{ip_address}} -p {{port}}`
- Execute script

mitmproxy -s {{script.py}} -p 9092


- Connect to proxy

`mitmproxy --mode upstream:https://HOSTNAME:PORT --upstream-auth USER:PASSWORD`


