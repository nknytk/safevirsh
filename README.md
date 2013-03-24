This is a wrapper for virsh command.
Managing kvm virtual machine through safevirsh can prevent unintended over-commit of resource.
safevirsh works only for kvm, not for Xen.

Edit following setting before use.
GUEST_CONF_DIR: Path where VM setting XML files are.
GUEST_IMG_PARTITON: Path where VM images are.

Acceptable Commands:
  list
    -> List running VMs with commited resource.
  list --all
    -> List all VMs including shut domain with commited resource.
  list --autostart
    -> List VMs in auto-start list with commited resource.
  setvcpus id_or_domain-name cpunum
    -> Set domain's VCPU to cpunum.
  setmem id_or_domain_name memoryGB
    -> Set domain's memory to cpunum.
  start domain-name
    -> Start domain.
  autostart domain-name
    -> Mark domain as autostart.
