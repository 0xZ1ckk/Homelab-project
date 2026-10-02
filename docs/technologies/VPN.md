The VPN server used is IPsec, it was set using the auto setup script from [this repo](https://github.com/hwdsl2/setup-ipsec-vpn). Not much to say here, the script sets everything up and outputs a digital certificate that is then used to generate a key and other certificates. These ones are used on client side to authenticate against the server. To make the VPN server accessible from the internet, i've enabled port forwarding on my home router.

(add image here)

All connections coming to UDP ports 500 and 4500 from the internet are forwarded to the VPN server.

The VPN server is hosted on a Raspberry Pi host at the address 192.168.1.88, in the subnet containing my personal home devices. I will probably move it to a separate subnet. It used to be on a ubuntu VM on the ESXI host but i moved it so that i can reboot the server or change its network settings withtout losing connection and cutting myself out. 

