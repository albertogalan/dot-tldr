# dd

> Convert and copy a file.

- Make a bootable usb drive from an isohybrid file (such like archlinux-xxx.iso) and show the progress:

`dd if={{file.iso}} of=/dev/{{usb_drive}} status=progress`

- Clone a drive to another drive with 4MB block, ignore error and show progress:

`dd if=/dev/{{source_drive}} of=/dev/{{dest_drive}} bs=4M conv=noerror status=progress`

- Generate a file of 100 random bytes by using kernel random driver:

`dd if=/dev/urandom of={{random_file}} bs=100 count=1`

- Benchmark the write performance of a disk:

`dd if=/dev/zero of={{file_1GB}} bs=1024 count=1000000`

- Check progress of an ongoing dd operation (Run this command from another shell):

`kill -USR1 $(pgrep ^dd)`
- Write raw data blocks over ssh
`https://www.ndchost.com/wiki/server-administration/netcat-over-ssh`
`dd if=/dev/{{source_drive}} ssh | {{HOST}} dd of=/dev/{{source_drive}}`


- dd over nc + bzip 73% faster than ssh
`on HOST B`
`dd nc -l 19000|bzip2 -d | dd bs=16M of=/dev/{{source_drive}}`
`on HOST A`
`dd bs=16M if=/dev/{{source_drive}}|bzip2 -c|nc $HOST 19000`

