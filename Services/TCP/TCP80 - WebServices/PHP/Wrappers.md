#vulnerability

# Wrappers
## What is Wrappers?
PHP comes with many built-in wrappers for various URL-style protocols for use with the filesystem functions.
Basicallly it can include files, but in a `cyber` way.

## What does Wrappers give me?
* Local file inclusion! fun stuff

## Any documentation on Wrappers?
[PHP - Supported Protocols and Wrappers](https://www.php.net/manual/en/wrappers.php)


## How do I verify that a target is vulnerable?
* Find a maymay parameter in PHP
* throw it at it.
OR
* use `ath3no-dotdotpwn` (TODO)

## How do I use Wrappers?
Example:
`http://timing.htb/image.php?img=php[]()://filter/convert.base64-encode/resource=/etc/passwd`

