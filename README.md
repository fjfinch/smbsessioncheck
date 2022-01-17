# domcheck
Small python script that checks for null session and guest account on a Windows machine. It uses the SMB protocol. (Can also enumerate Linux via Samba).

Note for Windows: can't ping the box? Then probably 'File and printer sharing' is disabled and you can't use this script.

## Install dependencies
It uses the impacket libraries to connect to a machine:

```
apt install python3-impacket
```

## Run
This script requires an IP address as input:

```
python3 domcheck <IP>
```

## ToDo
* Output what registries/policies/smb.conf have been set to disable null/guest
* Guest check can fail with a different language (ex. the string 'Anonymous Logon' can be different)
