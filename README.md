# Migrate-VMware-VM-to-VirtualBox
Here are the steps I took to migrate VMware VM to VirtualBox:

1. Consolidate the snapshots and disk image files, by creating a new vmdk file (Type 0 is single growable):
    /Applications/VMware\ Fusion.app/Contents/Library/vmware-vdiskmanager -r <current snapshot vmdk file> -t 0 <new vmdk file>
2. Create a VirtualBox VM, but do not create a new virtual HD.
3. Copy/move the converted vmdk file to the new VirtualBox VM directory, and add it to the VM.
4. Boot the VM. It should work.
5. Remove the VMware tools with `vmware-tools-uninstall.pl` (as root)
6. Install the VirtualBox guest extension.
7. Done.
