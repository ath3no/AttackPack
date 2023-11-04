#tool

# DotDotPwn
## What is DotDotPwn?
DotDotPwn is a path traversal scanning tool for use on websites.

## How do I use DotDotPwn?
`perl dotdotpwn.pl -m http-url -u "http://hackmedia.htb/display/?page=TRAVERSAL" -b -s -k "root:" -f /etc/passwd`

## Any documentation on DotDotPwn?
TODO

## Any caveats I should be aware of?
* Does not catch Unicode Normalization vulnerabilities.
	* Patched in `ath3no-dotdotpwn`, under the `unicode` lab in Documents/htb.