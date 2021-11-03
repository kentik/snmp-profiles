---
name: SNMP Profile Request
about: Request a new profile be created for a device
title: "[Missing SNMP Profile]"
labels: profile
assignees: ''

---

*Please add the Device Vendor and Model to the issue title as well*

Device Vendor: 

Device Model: 

System Object Identifier (SysOID): 

List of critical metrics that you expect in the profile (does not need to be all-inclusive, just a general idea of your expectations):

 - 
 -
 -

**Please provide a [public gist](https://gist.github.com/) with a sanitized SNMP walk of the device** *(sensitive information removed)*

Gist Link: 

---
Example SNMP walk commands:
```
# v2c example
snmpwalk -v 2c -On -c $COMMUNITY_STRING $IP_ADDRESS . >> $DEVICE_TYPE.out

# v3 example
snmpwalk -v3 -On -l authPriv -u $USERNAME -a MD5|SHA -A $AUTH_PASS -x DES|AES -X $PRIV_PASS $IP_ADDRESS . >> $DEVICE_TYPE.out
```