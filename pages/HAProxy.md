## Shared Configuration
	- ip:: 10.0.10.27 (Future: 10.0.10.3)
- ## Frontends
	- ### Library
		- |Listen Address|Port|SSL Offloading|
		  |10.0.10.27|443||
		- |Rule|Backend|
		  ||((681ebc8d-6c90-4b87-992c-b706a3a69c92))|
		  ||((681ebc28-d902-4b1a-9eca-e7445cdb3aeb))|
		  ||((681ebc28-d902-4b1a-9eca-e7445cdb3aeb))|
		  ||((681ebc40-7865-44b9-8583-c27064d0fd45))|
		  ||((681ebc16-85cf-44a3-b5e8-6af4e45ad73d))|
		  ||((681ebfd1-46be-4a19-aadd-aa6a6edee0f4))|
		  ||((681ebfdb-afba-474e-8858-f717bbb60a30))|
		  |Default|((681ebc8d-6c90-4b87-992c-b706a3a69c92))|
	- ### Websites
- ## Backends
	- Backup-Server
	  id:: 681ebc16-85cf-44a3-b5e8-6af4e45ad73d
	- Gitlab-Backend
	  id:: 681ebc28-d902-4b1a-9eca-e7445cdb3aeb
	- Gitlab-Backend-DockerReg
	  id:: 681ebc40-7865-44b9-8583-c27064d0fd45
	- Talos-Dev-API
	- Talos-Prod-API
	- Talos-Sandbox-API
	- Proxmox-Servers
	  id:: 681ebc8d-6c90-4b87-992c-b706a3a69c92
	- Suwayomi
	  id:: 681ebfd1-46be-4a19-aadd-aa6a6edee0f4
	- Calibre-web
	  id:: 681ebfdb-afba-474e-8858-f717bbb60a30