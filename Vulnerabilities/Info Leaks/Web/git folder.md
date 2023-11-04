#vulnerability

# git folder
## What is git folder?
A `.git` folder hosts all git-related info a repo has. This means you can access everything git if you have it :)

## What does git folder give me?
* Commit messages
* Branches
* Objects
	* packed archives of the code at that commit!
		* use `git unpack-objects < PACK_FILE` to get the code!

## Any documentation on git folder?
TODO

## How do I verify that a target is vulnerable?
Find a directory that might host code, and try to access `/DIR/.git/HEAD`
you might find it.

## How do I use git folder?
If you find a weird directory that might host code, try scanning for a .git folder in it
References to such places:
* Hackthebox - Vessel
* Hackthebox - UpDown
