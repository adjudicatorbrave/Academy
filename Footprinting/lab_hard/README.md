
# Footprinting Lab - Hard

## Information Gathering

* Ran a NMAP scan on the box and found the following ports open:
  * 22 - ssh
    * SSH-2.0-OpenSSH_8.2p1 Ubuntu-4ubuntu0
    * Authentication methods supported are publickey and passwords.
  * 143 and 993 - Dovecot imapd
  * 118 amd 995 - Dovecot pop3
  * 62 - DHCP
  * 161 - net-snmp SNMPv3 server
    * `onesixtyone -c ~/HTB/Tools/SecLists/Discovery/SNMP/snmp-onesixtyone.txt 10.129.71.172`
    * `10.129.71.172 [backup] Linux NIXHARD 5.4.0-90-generic #101-Ubuntu SMP Fri Oct 15 20:00:55 UTC 2021 x86_64`
    * `snmpwalk -v2c -c backup 10.129.71.172 > snmpwalk_output`
    * Captured username and password `tom NMds732Js2761"`

  
* Host Iis Unbuntu and name is NIXHARD
