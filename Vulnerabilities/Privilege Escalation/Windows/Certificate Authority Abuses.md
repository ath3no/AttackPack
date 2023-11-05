#vulnerability

# Certificate Authority Abuses
## What are Certificate Authority Abuses?
A Windows Domain Controller is also a Certificate Authority, and certificates are an alternative method to log into Windows machines. If you can generate a certificate with other permissions than your own, you might be able to extract hashes of other users and PTH to them!

## What do Certificate Authority Abuses give me?
A method of extracting hashes of other users, if you're lucky.

## Any documentation on Certificate Authority Abuses?
[Certipy - GitHub](https://github.com/ly4k/Certipy)

## How do I verify that a target is vulnerable?
* Use Certify.exe to dump vulnerabilities from the machine.
* Use certipy's walkthrough to verify methods.

## How do I use Certificate Authority Abuses?
Use the GitHub. It's mostly black magic.