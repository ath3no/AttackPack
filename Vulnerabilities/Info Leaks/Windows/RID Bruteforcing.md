#vulnerability

# RID Bruteforcing
## What is RID Bruteforcing?
RID Bruteforcing (or RID cycling) is an attack to discover entities on Windows domains. It cycles through RIDs (or Relative Identifiers) with an anonymous session in order to leak domain groups and users.

## What does RID Bruteforcing give me?
A list of domain group names and usernames.

## Any documentation on RID Bruteforcing?
TODO

## How do I verify that a target is vulnerable?
* open LDAP port
* login method
	* anonymous login possible (can be verified with SMB anonymous login)
	* domain credentials

## How do I use RID Bruteforcing?
You can use `crackmapexec` to carry this out:
```bash
crackmapexec smb manager.htb -u anonymous -p '' --rid-brute
```