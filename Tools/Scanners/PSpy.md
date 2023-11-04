#tool

# PSpy
## What is PSpy?
pspy is a command line tool designed to snoop on processes without need for root permissions. It allows you to see commands run by other users, cron jobs, etc. as they execute.

## How do I use PSpy?
Run `./pspy`
You can run `pspy --help` to learn about the flags and their meaning. The summary is as follows:

- `-p`: enables printing commands to stdout (enabled by default)
- `-f`: enables printing file system events to stdout (disabled by default)
- `-r`: list of directories to watch with Inotify. pspy will watch all subdirectories recursively (by default, watches /usr, /tmp, /etc, /home, /var, and /opt).
- `-d`: list of directories to watch with Inotify. pspy will watch these directories only, not the subdirectories (empty by default).
- `-i`: interval in milliseconds between procfs scans. pspy scans regularly for new processes regardless of Inotify events, just in case some events are not received.
- `-c`: print commands in different colors. File system events are not colored anymore, commands have different colors based on process UID.
- `--debug`: prints verbose error messages which are otherwise hidden.

## Any documentation on PSpy?
[PSpy - GitHub](https://github.com/DominicBreuker/pspy)

## Any caveats I should be aware of?
TODO