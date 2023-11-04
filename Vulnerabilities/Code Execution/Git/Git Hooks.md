#vulnerability

# Git Hooks
## What is Git Hooks?
Git hooks are hooks that are ran by git when actions are made using the git client.

## What does Git Hooks give me?
Git hooks can run bash code when the git client is used.

## Any documentation on Git Hooks?
[Git Hooks - Git Documentation](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks)

## How do I verify that a target is vulnerable?
A target that uses git as root, most likely as a cron job.

## How do I use Git Hooks?
Create a bash script with a specific name under `~/.git/hooks`.
execute it as root. :)