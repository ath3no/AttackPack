#vulnerability

# ASREPRoasting
## What is ASREPRoasting?
ASREPRoasting is a way to extract a password hash of a user based on the `Dont-Require-Preauth` flag in Kerberos.

## What does ASREPRoasting give me?
A valid Kerberos hash, which can be offline-cracked.

## Any documentation on ASREPRoasting?
[ASREP Roasting - HackTricks](https://book.hacktricks.xyz/windows/active-directory-methodology/asreproast)

## How do I verify that a target is vulnerable?
Use `impacket-GetNPUsers` with a list of usernames.

## How do I use ASREPRoasting?
`impacket-GetNPUsers -usersfile USERS_LIST_FILE -dc-ip X.X.X.X DOMAIN.NAME/`