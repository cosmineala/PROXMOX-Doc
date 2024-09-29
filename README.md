# PROXMOX-Doc

# Create Business Central Container on Windows 11 on PROXMOX

## Config VM to to suport containers (nested virtualization)

If this step is not completed the VM will be bricked

File is located at:
```
/etc/pve/qemu-server/<VM_NUMBER>.conf
```

change `cpu` propety to `host,hidden=1,flags=-hypervisor;+svm`

```
cpu: host,hidden=1,flags=-hypervisor;+svm
```


## Enable Remote Desktop
Settings > System > Remoate Desktop

set Remote Desktop on

Remote Desktop Users > add your user
and note the local domain