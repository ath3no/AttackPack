#vulnerability

# SMB Hash-Grab
## What is SMB Hash-Grab?
SMB Hash-grab allows you to grab an NTLM hash of a Windows user by making them authenticate with you using SMB.

## What does SMB Hash-Grab give me?
An NTLM hash you can PTH with, or crack with `hashcat`

## Any documentation on SMB Hash-Grab?
TODO

## How do I verify that a target is vulnerable?
If you can read a file from a remote smb server, it's vulnerable.

## How do I use SMB Hash-Grab?
* `sudo responder`
* make the target request anything from you using SMB
* done!