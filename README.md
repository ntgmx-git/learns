# learns
## The guix path
Would it be able to manage some reproducible workflow with guix? Here are the steps I think I will follow to get "on-demand" VMs. 

1. Create a simple vm config.scm
2. Check with guix lint and guix style
3. Test the VM with guix vm 
4. Create a bootable disk with guix system image
5. Export the instance and run it somewhere (virt-manager localy, Proxmox Virtual Environment remotely)
6. Manage updates from the guix system by:
6.1 Run guix pull and guix deploy 
6.2 Update configuration file (new packages, config changes, new services)
7. Monitor VMs thanks to guix graph, size, challenge, and processes? 
8. Start over again.
