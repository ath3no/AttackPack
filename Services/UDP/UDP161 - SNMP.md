#service 

# UDP161 - SNMP
## What is SNMP?
Simple Network Management Protocol.

Wikipedia:
Simple Network Management Protocol is an Internet Standard protocol for collecting and organizing information about managed devices on IP networks and for modifying that information to change device behaviour.

SNMP stores data in a tree, and accesses them with tree identifiers called OIDs.

![OID tree structure](https://1517081779-files.gitbook.io/~/files/v0/b/gitbook-28427.appspot.com/o/assets%2F-L_2uGJGU7AVNRcqRvEi%2F-MAwjRVVe_fE3LEMWuKt%2F-MAx-w1fbcPOpLV-IoIz%2FSNMP_OID_MIB_Tree.png?alt=media&token=018f6590-94ce-4244-8fd4-0c3fb83e8035)



## How do I connect to SNMP?
* `snmpbrute` can bruteforce the commstring using a dictionary attack on common commstrings.
* `snmpwalk` can trace an entire infotree and dump its contents + OIDs.

## Any documentation on SNMP?
[HackTricks - Pentesting SNMP](https://book.hacktricks.xyz/pentesting/pentesting-snmp)
[Rapid7 - SNMP Data Harvesting During PenTesting](https://www.rapid7.com/blog/post/2016/05/05/snmp-data-harvesting-during-penetration-testing/)
[OIDInfo - Every OID's meaning](http://www.oid-info.com/cgi-bin/display?tree=#focus)


## How do I collect info from SNMP?
TODO

## How do I run code on SNMP?
TODO