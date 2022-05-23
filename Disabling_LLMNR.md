# How and why to disable LLMNR 
A threat actor can exploit LLMNR to capture usernames and passwords on a local network.
## What is LLMNR
Link-Local Multicast Name Resolution or in short LLMNR is a protocol that allows name resolution without a DNS server.
LLMNR is a component of Microsoft Windows machines.
## Threat model
Threat actors can listen, broadcast and respond on a network to UDP/5355 LLMNR.
Thus, a threat actor can pretend that he knows the location of the requested host.
## How to disable LLMNR in Linux
>nano /etc/systemd/resolved.conf
Edit the line:LLMNR=resolve to LLMNR=no
>reboot

