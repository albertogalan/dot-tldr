# lxc

> Manage Linux containers using the lxd REST API.
> Any container names or patterns can be prefixed with the name of a remote server.

- List local containers matching a string. Omit the string to list all local containers:

`lxc list {{match_string}}`

- List images matching a string. Omit the string to list all images:

`lxc image list [{{remote}}:]{{match_string}}`

- Create a new container from an image:

`lxc launch [{{remote}}:]{{image}} {{container}}`

- Start a container:

`lxc start [{{remote}}:]{{container}}`

- Stop a container:

`lxc stop [{{remote}}:]{{container}}`

- Show detailed info about a container:

`lxc info [{{remote}}:]{{container}}`

- Take a snapshot of a container:

`lxc snapshot [{{remote}}:]{{container}} {{snapshot}}`
- port forwarding

`lxc config device add mycontainer myport80 proxy listen=tcp:0.0.0.0:80 connect=tcp:localhost:80`


- Turning a container into an image

`lxc publish {{container}} --alias {{image}}`


- Turn a past conatiner snapshot into a new image

`lxc publish {{container/xx-snapshot}} --alias {{image}}`


- creating docker container , makes priviledge
`lxc config set nestc1 security.nesting true`
`lxc config set nestc1 security.privileged true`
`sudo apt install docker.io`
`sudo adduser agalan docker`

- Push a file into container
`lxc image export ubuntu18`
`lxc file push file path/file`
- in the container
`lxc file import file path/file`


- enter in bash

`lxc exec crawler -- /bin/bash`


- launch new images on remote

lxc launch tuna-images:ubuntu/18.04 trig:u18


- Launch new image on remote

`lxc launch tuna:ubuntu/18.04 trig:u18`


- list images

`lxc image list tuna:`
`lxc image list images:`


