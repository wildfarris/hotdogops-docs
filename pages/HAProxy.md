## Frontends
	- ### Websites
		- |Listen Address|Port|SSL Offloading|
		  |10.0.10.27|443|Enabled|
		  |10.0.10.27|8443|Enabled|
		- |Rule|Backend|
		  |^proxmox(.lab)?\.phares\.io$|((681ebc8d-6c90-4b87-992c-b706a3a69c92))|
		  |^gitlab(.lab)?\.phares\.io(:443)?$|((681ebc28-d902-4b1a-9eca-e7445cdb3aeb))|
		  |^pages(.lab)?\.phares\.io$|((681ebc28-d902-4b1a-9eca-e7445cdb3aeb))|
		  |^backup(.lab)?\.phares\.io$|((681ebc16-85cf-44a3-b5e8-6af4e45ad73d))|
		  |Default|((681ebc8d-6c90-4b87-992c-b706a3a69c92))|
	- ### Talos-Sandbox
		- |Listen Address|Port|SSL Offloading|
		  |N/A|6443|Disabled|
		- |Rule|Backend|
		  |Default|((681ebc83-152f-4274-8649-58bf8187813d))|
	- ### Talos-Dev
		- |Listen Address|Port|SSL Offloading|
		  |10.0.10.200|6443|Disabled|
		- |Rule|Backend|
		  |Default|((681ebc4d-daf1-443b-84da-999ec993c48c))|
	- ### Talos-Prod
		- |Listen Address|Port|SSL Offloading|
		  |10.0.10.210|6443|Disabled|
		- |Rule|Backend|
		  |Default|((681ebc77-c6ee-4516-89c1-fbfb07a1bc27))|
	- ### Gitlab-DockerReg
		- |Listen Address|Port|SSL Offloading|
		  |10.0.10.27|5000|Enabled|
		- |Rule|Backend|
		  |Default|((681ebc40-7865-44b9-8583-c27064d0fd45))|
- ## Backends
	- Backup-Server
id:: 681ebc16-85cf-44a3-b5e8-6af4e45ad73d
		- health-check:: HTTP (GET)
		  backend-pass-thru:: ``timeout tunnel 3600s``
		- |Name|Address|Port|SSL|SSL Check|Weight|
		  |[[PBS]]|nas.lab.phares.io|8007|True|False||
	- Gitlab-Backend
id:: 681ebc28-d902-4b1a-9eca-e7445cdb3aeb
		- health-check:: HTTP (GET)
		- |Name|Address|Port|SSL|SSL Check|Weight|
		  |[[gitlab1]]|gitlab1.lab.phares.io|80|False|False||
	- Gitlab-Backend-DockerReg
id:: 681ebc40-7865-44b9-8583-c27064d0fd45
		- health-check:: Basic
		- |Name|Address|Port|SSL|SSL Check|Weight|
		  |[[gitlab1]]|gitlab1.lab.phares.io|5050|False|False|
	- Talos-Dev-API
id:: 681ebc4d-daf1-443b-84da-999ec993c48c
		- health-check:: Basic
		- |Name|Address|Port|SSL|SSL Check|Weight|
		  |[[talos-dev1]]|talos-dev1.lab.phares.io|6443|False|False||
		  |[[talos-dev2]]|talos-dev2.lab.phares.io|6443|False|False||
		  |[[talos-dev3]]|talos-dev3.lab.phares.io|6443|False|False||
	- Talos-Prod-API
id:: 681ebc77-c6ee-4516-89c1-fbfb07a1bc27
		- health-check:: Basic
		- |Name|Address|Port|SSL|SSL Check|Weight|
		  |[[talos-prod1]]|talos-prod1.lab.phares.io|6443|False|False||
		  |[[talos-prod2]]|talos-prod2.lab.phares.io|6443|False|False||
		  |[[talos-prod3]]|talos-prod3.lab.phares.io|6443|False|False||
	- Talos-Sandbox-API
id:: 681ebc83-152f-4274-8649-58bf8187813d
		- health-check:: Basic
		- |Name|Address|Port|SSL|SSL Check|Weight|
	- Proxmox-Servers
	  id:: 681ebc8d-6c90-4b87-992c-b706a3a69c92
		- health-check:: HTTP (GET)
		  persistence:: SSL-Session-ID (1h)
		  backend-pass-thru:: ``timeout tunnel 3600s``
		- |Name|Address|Port|SSL|SSL Check|Weight|
		  | [[proxmox1]] |10.0.10.11|8006|True|True||
		  | [[proxmox2]] |10.0.10.12|8006|True|True||
		  | [[proxmox3]] |10.0.10.13|8006|True|True||