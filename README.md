# domcheck
Small python script that checks for null session and guest account on a machine. It uses the SMB/Samba protocol to enumerate Windows/Linux.

## install dependencies
It uses the impacket libraries to connect to a machine:

```
apt install python3-impacket
```

## run
This script requires an IP address as input:

```
python3 domcheck <IP>
```

## ToDo
* Output what registries/policies/smb.conf have been set to disable null/guest
