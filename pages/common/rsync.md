# rsync

> Transfer files either to or from a remote host (not between two remote hosts).
> Can transfer single files, or multiple files matching a pattern.

- Transfer file from local to remote host:

`rsync {{path/to/file}} {{remote_host_name}}:{{remote_host_location}}`

- Transfer file from remote host to local:

`rsync {{remote_host_name}}:{{remote_file_location}} {{local_file_location}}`

- Transfer file in archive (to preserve attributes) and compressed (zipped) mode:

`rsync -az {{path/to/file}} {{remote_host_name}}:{{remote_host_location}}`

- Transfer a directory and all its children from a remote to local:

`rsync -r {{remote_host_name}}:{{remote_folder_location}} {{local_folder_location}}`

- Transfer only updated files from remote host:

`rsync -ru {{remote_host_name}}:{{remote_folder_location}} {{local_folder_location}}`

- Transfer file over SSH and show progress per file:

`rsync -e ssh --progress {{remote_host_name}}:{{remote_file}} {{local_file}}`

- Transfer file over SSH and show global progress:

`rsync -e ssh --info=progress2 {{remote_host_name}}:{{remote_file}} {{local_file}}`

- sudo privilege

`rsync --rsync-path="sudo rsync"  {{remote_host_name}}:{{remote_file}}`

- rsync through ssh

`  export RSYNC_CONNECT_PROG='ssh proxyhost nc %H 873'`
`  rsync -av targethost1::module/src/ /dest/`
`  rsync -av rsync:://targethost2/module/src/ /dest/ `

- rsync through ssh with nc  and config

`Host target`
`  ProxyCommand nohup ssh middle nc -w1 %h %p`
`  HostName target`
`  User target_user`
`more examples https://rsync.samba.org/firewall.html`
