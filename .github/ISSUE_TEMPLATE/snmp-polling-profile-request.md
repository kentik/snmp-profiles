---
name: SNMP Polling Profile Request
about: Request a new polling profile be created for a device
title: "[Missing SNMP Polling Profile]"
labels: profile
assignees: ''

---

[NOTE]: # ( ^^ Please add the Device Vendor and Model in the title above. ^^ )

Device Vendor: 

Device Model: 

[NOTE]: # (If you do not know your SysOID, it can be gathered from the SNMP walk you provide at the end of this issue. It is the value of this OID in the SYSTEM-MIB: `1.3.6.1.2.1.1.2.0`)

System Object Identifier (SysOID): 

List of critical metrics that you expect in the profile (does not need to be all-inclusive, just a general idea of your expectations):

 - 
 -
 -
 
If there is a New Relic technical support case related to this request, please provide the case number:

**Please provide a [public gist](https://gist.github.com/) with a sanitized** *(sensitive information removed)* **SNMP walk of the device. Providing MIB files is not a substitute for an SNMP walk and failure to provide one here will result in delays for closing this issue. The output of these commands shows the "true story" of what a device will respond to in SNMP and is used to ensure that our profiles are efficient and accurate for your devices.**

Gist Link: 

---
Example SNMP walk commands:
```
# v2c example
snmpwalk -v 2c -t 10 -On -c $COMMUNITY_STRING $IP_ADDRESS . >> snmp_walk.out

# v3 example
snmpwalk -v3 -t 10 -l authPriv -u $USERNAME -a MD5|SHA -A $AUTH_PASS -x DES|AES -X $PRIV_PASS -ObentU -Cc $IP_ADDRESS . >> snmp_walk.out
```
