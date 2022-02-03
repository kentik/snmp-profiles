---
name: SNMP Traps Profile Request
about: Request a new Traps profile be created for a device
title: "[Missing SNMP Traps Profile]"
labels: snmp-trap-profile
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

**Please provide a [public gist](https://gist.github.com/) with BOTH a sanitized** *(sensitive information removed)* **PCAP capture of SNMP Trap samples for the device and the MIB file(s) that define the Traps this device will support.**

**The MIB file will give us the enumerated names of the metrics you wish to collect, while the output of the packet capture shows the "true story" of what a device will ship via SNMP Traps and is used to ensure that our profiles are efficient and accurate for your devices.**

Gist Link: 

---
Example of creating PCAP with the `tcpdump` utility:
```
sudo tcpdump -s 0 port 162 -w snmpTraps.pcap
```
---
To check if `tcpdump` is available on your system:
```
tcpdump --version
```

Output Example
```
tcpdump version 4.9.3
libpcap version 1.9.1
LibreSSL 2.8.3
```

To install `tcpdump`:
```
# Ubuntu / Debian
sudo apt update && sudo apt install tcpdump

# CentOS/Fedora
sudo yum install tcpdump
```
