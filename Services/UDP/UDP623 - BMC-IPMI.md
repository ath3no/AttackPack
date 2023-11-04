#service

# UDP623 - BMC/IPMI
## What is BMC?
Baseboard Management Controllers (BMCs) are a type of embedded computer used to provide out-of-band monitoring for desktops and servers. These products are sold under many brand names, including HP iLO, Dell DRAC, Sun ILOM, Fujitsu iRMC, IBM IMM, and Supermicro IPMI. BMCs are often implemented as embedded ARM systems, running Linux and connected directly to the southbridge of the host system's motherboard.
## How do I connect to BMC?
* port 623 on UDP - uses the IPMI protocol
* `msfconsole` -> `search ipmi` 
* `ipmitool`
* Other methods are listed in the pentest guide.
In general, there's a cool vuln called Cipher 0 which connects to the BMC given just a valid username (use `ipmitool -C 0` to exploit).

## Any documentation on BMC?
[Pentester's guide to IPMI](https://www.rapid7.com/blog/post/2013/07/02/a-penetration-testers-guide-to-ipmi/)
[HackTricks - port 623](https://book.hacktricks.xyz/pentesting/623-udp-ipmi)

## How do I collect info from BMC?
You can collect many pieces of info on the host, but the most important one is a hash-leak.

## How do I run code on BMC?
AFAIK you can't natively run *code* using a BMC, but you can:
* hijack a session using the serial port
* reboot the machine into a shell
Both are mentioned in the Pentester's guide listed in the documentation.