# How to install correctly virt-manager on Arch Linux 

I wrote this to remember how to install fully virt-manager on Arch Linux, because there are extra steps than just downloading the packages.

```bash
sudo pacman -Syu --needed virt-manager qemu-desktop qemu-full libvirt edk2-ovmf dnsmasq vde2 bridge-utils iptables-nft dmidecode 
# to be able to connect to QEMU/KVM from virt-manager
sudo systemctl enable --now libvirtd.service
sudo usermod -aG libvirt $USER
# to get NAT working
sudo virsh net-autostart default
sudo virsh net-start default
```

# Additionals thing to install in the VM

Install spice-vdagent inside the VM to get the VM to autoresize to the size of the window and reboot the VM (for QEMU/KVM).

```bash
# for ubuntu and debian
sudo apt install spice-vdagent
# after installing it, you just need to reboot the machine and select auto-resize VM in the "View" submenu of Virt-manager
```

# References

https://discovery.endeavouros.com/applications/how-to-install-virt-manager-complete-edition/2021/09/

https://docs.remnux.org/install-distro/get-virtual-appliance#hypervisor-requirements
