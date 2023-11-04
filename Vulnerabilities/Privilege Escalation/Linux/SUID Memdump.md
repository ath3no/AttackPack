#vulnerability

# SUID Memdump
## What is SUID Memdump?
SUID Memdump is a technique to leak information that is inaccessible in the current user context.
Essentially, it consists of purposefully crashing the running process of a SUID binary, so you receive a coredump of the process and can look inside the memory snapshot.

## What does SUID Memdump give me?
This technique can help you leak file contents and program outputs that are inaccessible just by using the SUID binary.

## Any documentation on SUID Memdump?
[Openwall - Core-dump handing issues with SUID binaries](https://www.openwall.com/lists/oss-security/2021/10/20/2)


## How do I verify that a target is vulnerable?
If you know that a SUID program is reading info you want and can't get, and the process is dumpable (defined in the code as a syscall, probably accessible through IDA), this technique can be used.

From the Secret HTB writeup - `This is usually not enabled by default.`

From the Openwall docs, although more complex:
```
To exploit this behavior, we first had to find a suid binary that meets the
following requirements:

1. A root suid binary.
2. Sets uid and gid to 0 (setuid(0) and setgid(0) are called).
3. Uses execve.
```

## How do I use SUID Memdump?
* run the SUID binary and get to the flow where the info you want is loaded into memory
* crash the process with `kill -SIGSEGV <pid>` -  this will cause a coredump
* the crash dump is saved at `/var/crashes`
* exfil the crash dump (or keep it on the machine if you're feeling extra-skiddy)
* use `apport-unpack <crashfile> /tmp/crash-report` 
* `cd /tmp/crash-report`
* have fun with the files!