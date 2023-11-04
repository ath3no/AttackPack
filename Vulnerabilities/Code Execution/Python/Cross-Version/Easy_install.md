#vulnerability

# Easy_install
## What is Easy_install?
Easy_install is a python package installer.

## What does Easy_install give me?
Code execution with process privileges.

## Any documentation on Easy_install?
TODO

## How do I verify that a target is vulnerable?
If you have access to the `easy_install` command, you're golden. If you have `sudo -l` aceess for it, even better :)

## How do I use Easy_install?
* Create a `setup.py` file in a new directory that runs the desired code
	* `bash` shell?
	* Implant? `Meterpreter`? `Brute`? `Grunt`?
	* A custom script?
* run `easy_install .`
* Done!