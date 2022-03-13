# Cisco IOS

## Manual

Enter ? for all available commands
exp. show ?

## User Exec Mode [Device>]

Kaum Rechte für irgendwas

## Priviledged Exec Mode [Device#] enable, disable

* show hosts
* show users
* show protocol
* show running-config
* show startup-config
* copy running-config startup-config
* show interface
* show ip interface brief
* ping ip $ip-addr

## Global Config [Device(config)#] config terminal, exit

* router rip
* hostname Switch1
* enable password $password, no enable password
* ip route $dest $mask $next_hop [0.0.0.0 0.0.0.0 for default route]

## Interface Config [Device­(co­nfi­g-if)#] interface $interface 0/0, end/exit

Interfaces:

* Ethernet
* Fast Ethernet
* Gigabit Ethernet
* Dial interfaces
* Serial interfaces
* Virtual or logical interfaces
* Tunnel interfaces

Commands:

* no shutdown (turns on the interface)
* shutdown (turns of the interface)
* ip address IP Subnet-Mask
* mac-address 0054.67FE.8CD4

## Line Config [Device­(co­nfi­g-line)] line console 0

Terminal settings

* password $passsword


Priviledged Exec Mode --> Global Config Mode
Router Config Mode --> Global Config Mode
Line Config Mode --> Global Config Mode

'enable' for priviledged exec mode
'exit' for Global Config Mode

Console port: seriell, asynchron

Cisco IOS: traceroute IP_ADDRESS
Unix: traceroute IP_ADDRESS
Windows: tracert IP_ADDRESS
