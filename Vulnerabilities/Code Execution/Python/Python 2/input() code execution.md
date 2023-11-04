#vulnerability

# input() code execution
## What is input() code execution?
Given user input through `input()`, a user can gain bypasses/code execution.

## What does input() code execution give me?
RCE :)

## Any documentation on input() code execution?
Here. Nothing else is really good.

## How do I verify that a target is vulnerable?
* A SUID python process
* A way to enter a string into `input()` to it

## How do I use input() code execution?
* Get to the `input()`
* Depends on target
	* if creds bypass is your thing, input the password variable name, usually `password`
		* This will be parsed at runtime and point to the variable!
	* If code execution is your thing, find a gadget that runs code!
		* Generic gadget: `__import__("os").system("/bin/bash")`
		* If \_\_import\_\_ is blocked, find a specific gadget:
			* `requests`: `requests.utils.socket.os.execv("/bin/bash", ["1"])`