The Dell server is running a ESXi hypervisor managed through the web interface. There's currently 6 VMs on it. On the networking side, two port groups where created, an "internal" one and an "external" one. The ESXi management interface and the VyOS router external interface use the external port group that thus mimics an external network that sits outside. The router also works as a firewall and filters the traffic coming from the external network into the internal one. The remaining VMs were all assigned the internal port group and thus belong to the internal network. In reality the server uses only one network adapter. 



### Possible upgrades 
- Installing VMWare vCenter for host management
