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
		  |^library(.lab)?\.phares\.io:8443$|((681ebfd1-46be-4a19-aadd-aa6a6edee0f4))|
		  |^library(.lab)?\.phares\.io$|((681ebfdb-afba-474e-8858-f717bbb60a30))|
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
	- ### Library
		- |Listen Address|Port|SSL Offloading|
		  |10.0.10.27|80|N/A|
		- |Rule|Backend|
		  |Default|((681ebfdb-afba-474e-8858-f717bbb60a30))|
- ## Backends
	- Backup-Server
	  id:: 681ebc16-85cf-44a3-b5e8-6af4e45ad73d
		-
	- Gitlab-Backend
	  id:: 681ebc28-d902-4b1a-9eca-e7445cdb3aeb
		-
	- Gitlab-Backend-DockerReg
	  id:: 681ebc40-7865-44b9-8583-c27064d0fd45
		-
	- Talos-Dev-API
	  id:: 681ebc4d-daf1-443b-84da-999ec993c48c
		-
	- Talos-Prod-API
	  id:: 681ebc77-c6ee-4516-89c1-fbfb07a1bc27
		-
	- Talos-Sandbox-API
	  id:: 681ebc83-152f-4274-8649-58bf8187813d
		-
	- Proxmox-Servers
	  id:: 681ebc8d-6c90-4b87-992c-b706a3a69c92
		-
	- Suwayomi
	  id:: 681ebfd1-46be-4a19-aadd-aa6a6edee0f4
		-
	- Calibre-web
	  id:: 681ebfdb-afba-474e-8858-f717bbb60a30
		- ```
		  mode			http
		  id			109
		  log			global
		  http-check		send meth GET
		  timeout connect		30000
		  timeout server		30000
		  retries			3
		  load-server-state-from-file	global
		  option			httpchk
		  timeout tunnel 3600s
		  ```