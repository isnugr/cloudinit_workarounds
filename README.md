
# A minimal feature set workaround to initialize OPNsense images in Proxmox.

## Usage
* Copy the directory `opnsense-cloudinit` into the target image folder `/root/`
* In target image execute: 
	* `echo /root/opnsense-cloudinit/opnsense-cloudinit > /usr/local/etc/rc.syshook.d/start/99-cloudinit` 
	* `chmod +x /usr/local/etc/rc.syshook.d/start/99-cloudinit`
	* `chmod -R u+x /root/opnsense-cloudinit/`

