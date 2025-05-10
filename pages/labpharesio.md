## Hosts
- {{embed [[proxmox1]]}}
- hosts:: [[proxmox1]], [[proxmox2]], [[proxmox3]]
  hosted-services:: [[ceph]]
- ## HA Groups
	- PVE1
		- priority-config:: 1: [[proxmox1]] , 2: [[proxmox2]], [[proxmox3]]
		  assigned-vms:: [[talos-dev1]], [[talos-dev4]], [[talos-prod1]], [[talos-prod4]], [[talos-prod7]]
	- PVE2
		- priority-config:: 1: [[proxmox2]] , 2: [[proxmox1]], [[proxmox3]]
		  assigned-vms:: [[talos-dev2]], [[talos-dev5]], [[talos-prod2]], [[talos-prod5]], [[talos-prod8]]
	- PVE3
		- priority-config:: 1: [[proxmox3]] , 2: [[proxmox1]], [[proxmox2]]
		  assigned-vms:: [[talos-dev3]], [[talos-dev6]], [[talos-prod3]], [[talos-prod6]], [[talos-prod9]]
- ## Storage
	- ceph_pool
		- type:: ceph RBD
		  usage:: Disks (raw)
	- pvevm
		- type:: NFS [[NAS]] 
		  usage:: Disks (qcow2), ISO image, Container (raw), Snippets, Container template (tzst)
	- talos-sandbox
		- type:: ceph RBD
		  usage:: ceph-csi-rbd
	- talos-dev
		- type:: ceph RBD
		  usage:: ceph-csi-rbd
	- talos-prod
		- type:: ceph RBD
		  usage:: ceph-csi-rbd