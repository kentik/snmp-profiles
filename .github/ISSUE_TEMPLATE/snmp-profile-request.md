---
name: SNMP Profile Request
about: Request a new profile be created for a device
title: "[Missing SNMP Profile]"
labels: profile
assignees: ''

---

Device Vendor: 

Device Model: 

System Object Identifier (SysOID): 

List of MIBs expected: 


**If possible, please add a current SNMP walk of the device, with sensitive information removed**


```
# v2c example
snmpwalk -v 2c -On -c $COMMUNITY_STRING $IP_ADDRESS . >> $DEVICE_TYPE.out

# v3 example
snmpwalk -v3 -On -l authPriv -u $USERNAME -a MD5|SHA -A $AUTH_PASS -x DES|AES -X $PRIV_PASS $IP_ADDRESS . >> $DEVICE_TYPE.out
```
