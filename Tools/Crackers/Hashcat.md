#tool

# Hashcat
## What is Hashcat?
Hashcat is `john` on steroids - a hash cracker, with built in support for GPUs, optimized kernels, and very detailed configuration

## How do I use Hashcat?
* bruteforce: `hashcat -O -a 3 -m 16500 hash.txt ?l?l?l?l?l?l?l -i --increment-min=6`
* Dictionary attack: `hashcat -O -a 0 -m <hashtype> hash.txt /usr/share/wordlists/rockyou.txt`

## Any documentation on Hashcat?
The only important part you should have besides `hashcat --help` is the hashtypes, so you can use `nth` for most hashes, it'll tell you the name of the hash and the `hashcat` type.

If you wanna look up one manually or `nth` can't recognize the one you're looking for, use [this link](https://hashcat.net/wiki/doku.php?id=example_hashes) to `hashcat`'s docs.

## Any caveats I should be aware of?
* Hash cracking is **intense**, if it's not on `rockyou`, it's probably not the answer to a challenge. Then again, if you're doing actual pentesting, it's worth to have `hashcat` running in the background.