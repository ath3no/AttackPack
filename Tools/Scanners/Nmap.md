#tool

# Nmap
## What is Nmap?
Nmap is a network mapping tool.

I don't think I need to explain too much about it.

## How do I use Nmap?
* scan all TCP ports - `nmap -sC -sV <IP> -p 0-65535`
* scan UDP ports - `sudo nmap -sU -sC -sV <IP> -p 0-65535`
	* apparently faster way - `sudo nmap -sU -sV - 10.10.11.124 --min-rate 7500 -F`

## Any documentation on Nmap?
Not really, but `nmap --help` should be enough.

## Any caveats I should be aware of?
* In some super-rare cases, nmap may miss something. If you're out of ideas, scan again.
* nmap sends more than one packet per port. This may fuck-up port-knocking.