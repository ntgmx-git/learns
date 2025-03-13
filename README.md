# learns
## The guix path
### Workflow
Would it be able to manage some reproducible workflow with guix? Here are the steps I think I will follow to get "on-demand" VMs. 

1. Create a simple vm config.scm
2. Check with guix lint and guix style
3. Test the VM with guix vm 
4. Create a bootable disk with guix system image
5. Export the instance and run it somewhere (virt-manager localy, Proxmox Virtual Environment remotely)
6. Manage updates from the guix system by:
- Run guix pull and guix deploy 
- Update configuration file (new packages, config changes, new services)
7. Monitor VMs thanks to guix graph, size, challenge, and processes? 
8. Start over again.

### Instances
Respecting steps described in the previous section, I would like to describe how to manage: 
- A dummy "client" server that should at least be accessible via ssh and linked to a wireguard infrastructure
- A wireguard "server" (I know it does not exist with wireguard but still) or HUB or gateway, able to link peers and apply some monitoring & firewalling
- A web server
- A "backup" server that should be able to reach other servers and backup their related valuable data / files etc... Working with a pull (the backup server connects to the "content") method. 

## Deployment of guix on a non-guix server
