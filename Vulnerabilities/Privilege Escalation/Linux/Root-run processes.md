#vulnerability

# Root-run processes
## What is Root-run processes?
A root-run process is a process that is run by `root`. Not much more to it.

## What does Root-run processes give me?
If you can communicate with a process that is run by root (for example, a server), then you should look for CVEs for that service.

Alternatively, you can look for code execution vulns in it, since running code on a root process means running as root.

## Any documentation on Root-run processes?
Not really, pretty simple. Just run `ps fauxwww` to see which processes you might be able to take advantage of.

## How do I verify that a target is vulnerable?
Check online.

## How do I use Root-run processes?
Look it up, most of the time you'll find a public exploit you can use.