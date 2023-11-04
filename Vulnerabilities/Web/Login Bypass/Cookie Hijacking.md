#vulnerability

# Cookie Hijacking
## What is Cookie Hijacking?
Cookie hijacking is a way of gaining access to a user without a password. This can be through stealing a session token, breaking a JWT signature or more.

## What does Cookie Hijacking give me?
A way to access accounts you otherwise can't, and without a password!

## Any documentation on Cookie Hijacking?
Lots, look up online.

## How do I verify that a target is vulnerable?
If the authentication mechanism uses a token (which it should), and you can break its generation method, it should be vulnerable.

## How do I use Cookie Hijacking?
* first - identify the cookie structure
	* session cookies - try to decrypt them
	* JWT - look inside for good info - then try to break its signature with HackTricks' tutorials.