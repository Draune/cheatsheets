# How to install correctly virt-manager on Arch Linux 

I wrote this to remember how to install fully virt-manager on Arch Linux, because there are extra steps than just downloading the packages.

```bash
sudo pacman -Syu --needed virt-manager qemu-desktop libvirt edk2-ovmf dnsmasq vde2 bridge-utils iptables-nft dmidecode
# to be able to connect to QEMU/KVM from virt-manager
sudo systemctl enable --now libvirtd.service
# to get NAT working
sudo virsh net-autostart default
sudo virsh net-start default
```

## References

https://discovery.endeavouros.com/applications/how-to-install-virt-manager-complete-edition/2021/09/
