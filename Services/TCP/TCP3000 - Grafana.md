#service

# TCP3000 - Grafana
## What is TCP3000 - Grafana?
Grafana is a web dashboard and data source tool.

## How do I connect to TCP3000 - Grafana?
`http://<server>:3000` and authenticate, or use vulns.

## Any documentation on TCP3000 - Grafana?
look up `grafana`

## How do I collect info from TCP3000 - Grafana?
[CVE-2021-43978 - Unauthenticated Arbitrary File Read through Grafana](https://github.com/pedrohavay/exploit-grafana-CVE-2021-43798)

## How do I run code on TCP3000 - Grafana?
Using the above CVE, you can leak `grafana.db`, `/etc/passwd`, and `grafana.ini`, any of which might have information to help further your progress on the machine
* `grafana.db` - tables might have creds for other data sources on the server, like a MySQL server.
* `/etc/passwd` - local machine users
* `grafana.ini` - generic `admin` user creds for grafana's webUI, password in plaintext.