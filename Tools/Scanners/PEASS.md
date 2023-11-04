#tool

# PEASS
## What is PEASS?
PEASS is a privesc tool suite, including `linpeas` and `winpeas`, letting you scan for common LPE routes in a machine.

## How do I use PEASS?
* get a shell on the target machine
* upload the executable
* execute it and log it to a file
	* Linux: `linpeas.sh | tee linpeas_out`
	* PowerShell: `./winpeas.exe | tee -filepath winpeas_out.txt`
	* CMD: `./winpeas.exe > winpeas_out.txt`
		* Sadly, in CMD you cannot see the output as it's being written.
* exfil the output file
* to display the file with

## Any documentation on PEASS?
[PEASS - GitHub](https://github.com/carlospolop/PEASS-ng)

## Any caveats I should be aware of?
* Like any tool, this isn't a magic bullet, read the output carefully and decide what to do on your own.
* Sometimes, there's nothing in PEASS that can help you.
	* In that case, try to think of common, huge CVEs that can help you (e.g. sudoedit/PwnKit/PrintNightmare/ETERNALBLUE)