# ssh

> Secure Shell is a protocol used to securely log onto remote systems.
> It can be used for logging or executing commands on a remote server.

- Connect to a remote server:

`ssh {{username}}@{{remote_host}}`

- Connect to a remote server with a specific identity (private key):

`ssh -i {{path/to/key_file}} {{username}}@{{remote_host}}`

- Connect to a remote server using a specific port:

`ssh {{username}}@{{remote_host}} -p {{2222}}`

- Run a command on a remote server:

`ssh {{remote_host}} {{command -with -flags}}`

- SSH tunneling: Dynamic port forwarding (SOCKS proxy on localhost:9999):

`ssh -D {{9999}} -C {{username}}@{{remote_host}}`

- SSH tunneling: Forward a specific port (localhost:9999 to slashdot.org:80) 
- disabling pseudo-[t]ty allocation and executio[n] of remote commands:

`ssh -L {{9999}}:{{slashdot.org}}:{{80}} -N -T {{username}}@{{remote_host}}`

- SSH jumping: Connect through a jumphost to a remote server (Multiple jump hops may be specified separated by comma characters):

`ssh -J {{username}}@{{jump_host}} {{username}}@{{remote_host}}`

- Add identity key to agent and Forward to machine
`eval $(ssh-agent); ssh-add /home/agalan/.ssh/id_rsa`
`ssh -A {{username}}@{{remote_host}}`

- Connect through sockets

`ssh tornae.com -D 29828 -f -C -q -N`

- Create a ssh and vpn

`sudo sshuttle --dns -r tornae.com 0.0.0.0/0`

- Execute a bash command remotely

`ssh {{host}} bash -s < script.sh`


- An ssh tunnuel via multiple hops

`ssh http://serverfault.com/questions/287059/multiple-hops-tunnels-howto`
`Host internal.hostname.tld internal`
`User          merdely`
`  HostName      internal.hostname.tld`
`  ProxyCommand  ssh merdely@gateway.hostname.tld nc %h %p 2> /dev/null`
``
``
`Host cont1.lxc internal`
`  User          cbunker`
`  HostName      cont1.lxc`
`  ProxyCommand  ssh merdely@gateway.hostname.tld nc %h %p 2> /dev/null`

- An ssh tunnuel via two servers

`Host u0`
`HostName {{host}}`

`Host u1`
` ProxyCommand ssh -q u0 nc -q0 %h 22`

`Host u2`
` ProxyCommand ssh -q u1 nc -q0 %h 22`

`Host u3`
` ProxyCommand ssh -q u2 nc -q0 %h 22`


