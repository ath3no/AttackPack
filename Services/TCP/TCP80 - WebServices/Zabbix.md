#service
# Zabbix
## What is Zabbix?
Zabbix is an open-source monitoring solution, used from a web interface.

## How do I connect to Zabbix?
`http://server_ip_or_name/zabbix`
Alternate method:
`http://zabbix.{server_name}/`
`http://monitor.{server_name}/`
`http://monitoring.{server_name}/`

## Any documentation on Zabbix?
[Zabbix Download Page](https://www.zabbix.com/download) 
[Zabbix Takeover using scripts](https://www.whiteoaksecurity.com/blog/take-over-situations-part-1-zabbix/)

## How do I collect info from Zabbix?
You can get a lot of info from Zabbix, but it's better to just execute code if you get access to a server.

## How do I run code on Zabbix?
If you manage to get access to a Zabbix server, there's the link above.

If the Zabbix version is newer, there's a newer way - 
* create an Item by going to Hosts -> Items -> Create Item in the top right.
* in the Key field, type in `system.run[<COMMAND>, nowait]`
* Click "Test" -> "Get value and test"
* Bam, shell!