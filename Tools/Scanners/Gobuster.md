#tool

# Gobuster
## What is Gobuster?
Gobuster is a brute-force tool for websites. It can bruteforce:
* DNS servers
* VHosts
* Directories and pages in a website

## How do I use Gobuster?
* For website scanning - `gobuster dir --url <URL> --wordlist /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x <file_extensions>`
* For vhost scanning - 
	* `gobuster vhost --url <URL> --wordlist=/usr/share/wordlists/seclists/Discovery/DNS/subdomains-top1million-110000.txt | tee vhost_out.txt`
	* `cat vhost_out.txt | grep 200` to filter out noise if there is any.
* For DNS server scanning - 
	* `gobuster dns -d <domain> -w <wordlist> [-r <resolver>]`

## Any documentation on Gobuster?
* `gobuster --help`
* `gobuster <mode> --help` - for specific modes

## Any caveats I should be aware of?
* Sometimes `gobuster` is bad at filtering noise - that doesn't mean it's not working. Pipe the output to a file and `grep` to your heart's content.