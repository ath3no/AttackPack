#tool

# python pty bash tty
## What is python pty bash tty?
Python's PTY library can help you spawn a TTY shell instead of a "dumb" sh one.

## How do I use python pty bash tty?
`python3 -c 'import pty; pty.spawn("/bin/bash")'`

## Any documentation on python pty bash tty?
none really needed. Does what it says on the box.

## Any caveats I should be aware of?
* no *visual* autocomplete and history traversal
	* it does work, you'll just see the ANSI codes for the buttons you press.