VirtualBox allows you to run virtual machines on your computer. For example, you can run Linux or Windows as a <i>guest</i> on an Apple <i>host</i>.

# List vms

$ VBoxManage list vms



# Inspect specific VM

$ VBoxManage showvminfo "debian"



# Restart paused VM

$ VBoxManage controlvm "debian" resume





VirtualBox can create a local network, so that the different VMs can communicate. By default,  it uses the 10.0.2.0/24 IP block.

$ VBoxManage list natnets

NetworkName:    NatNetwork

IP:             10.0.2.1

Network:        10.0.2.0/24

IPv6 Enabled:   No

IPv6 Prefix:    

DHCP Enabled:   Yes

Enabled:        Yes

Port-forwarding (ipv4)

        Rule 1:tcp:[]:2222:[10.0.2.7]:22

loopback mappings (ipv4)

        127.0.0.1=2



However, because it is behind a local NAT, we have to forward ports explicitly if we want to connect from the outside:

$ VBoxManage natnetwork modify --netname NatNetwork -p "wiki:tcp:[]:3000:[10.0.2.101]:3000"

