# smbsessioncheck
Small python script that checks for a null session and an active guest account on a Windows machine. Great for initial enumeration without using a password. It uses the SMB protocol with RPC to enumerate the machine. (Can also enumerate Linux through Samba).

Note for Windows: can't ping the box? Then probably 'File and printer sharing' is disabled on the machine and you can't use this script.

## Install dependencies
It uses the impacket library to connect to a remote machine:

```
apt install python3-impacket
```

## Run
This script requires an IP address as input:

```
python3 smbsessioncheck <IP>
```

Output:

```
NetBIOS computer name	: FINCH-PC
NetBIOS domain name	: -
DNS host name		: finch-PC
DNS domain name		: -

Null session		: NO
Guest logon		: YES
```

## ToDo
* Output what registries/policies/smb.conf have been set to disable null/guest
* Guest check can fail with a different language (ex. the string 'Anonymous Logon' can be different)
