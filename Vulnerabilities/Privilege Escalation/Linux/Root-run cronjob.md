#vulnerability

# Root-run cronjob
## What is Root-run cronjob?
A cron job that is run by `root`.

## What does Root-run cronjob give me?
Either info leak or code execution, depends on implementation.

## Any documentation on Root-run cronjob?
TODO

## How do I verify that a target is vulnerable?
Use `pspy` to discover cron jobs while they run!

## How do I use Root-run cronjob?
* use `pspy` to find a cron job and what it does.
* try to find/guess its functionality
* exploit that functionality to open a shell/leak a file
* done!