- 10.0.10.0/24 ([Diagram]([[10.0.10.0/24 - Diagram]]))
	- 10.0.10.0/25
		- 10.0.10.0/26
			- 10.0.10.0/27
				- environment:: [[Infrastructure]]
				  static-hosts:: [[firewall]], [[HAProxy]], [[Switch]], [[syslog]], [[cloudflared]], [[cloudflared-ha]], [[proxmox1]], [[proxmox2]], [[proxmox3]], [[gitlab1]], [[gitlab-pages]], [[gitlab-runner]], [[amp1]] 
				  dynamic-ip-range:: N/A
			- 10.0.10.32/27
			  id:: 681d5322-3daf-4cb9-841a-9c488c7cbee8
				- 10.0.10.32/28
				  collapsed:: true
					- environment:: [[Lab-DHCP]] 
					  static-hosts:: N/A
					  dynamic-ip-range:: 10.0.10.33-10.0.10.46
				- 10.0.10.48/28
				  collapsed:: true
					- environment:: [[Sandbox]]
					  static-hosts:: [[sandbox.k8s.lab.phares.io]], [[talos-sandbox1]], [[sandbox-dns.k8s.lab.phares.io]]
					  dynamic-ip-range:: 10.0.10.57-10.0.10.63
					  id:: 681e3b94-6d10-495b-a6b8-6fa028546bea
		- 10.0.10.64/26
			- 10.0.10.64/27
			  id:: 681e3c8d-aa22-433c-98af-9fb2bee42e26
				- environment:: [[Dev]] 
				  static-hosts:: [[dev.k8s.lab.phares.io]], [[talos-dev1]], [[talos-dev2]], [[talos-dev3]], [[talos-dev4]], [[talos-dev5]], [[talos-dev6]], [[dev-dns.k8s.lab.phares.io]] 
				  dynamic-ip-range:: 10.0.10.81-10.0.10.87
			- 10.0.10.96/27
			  id:: 681e3ca3-b119-428e-aa1d-d4237db40740
				- environment:: [[Prod]] 
				  static-hosts:: [[prod.k8s.lab.phares.io]], [[talos-prod1]], [[talos-prod2]], [[talos-prod3]], [[talos-prod4]], [[talos-prod5]], [[talos-prod6]], [[talos-prod7]], [[talos-prod8]], [[talos-prod9]], [[prod-dns.k8s.lab.phares.io]] 
				  dynamic-ip-range:: 10.0.10.113-10.0.10.119
	- 10.0.10.128/25
		- 10.0.10.128/26
			- 10.0.10.128/27
			  collapsed:: true
				- environment:: 
				  static-hosts:: 
				  dynamic-ip-range::
			- 10.0.10.160/27
			  collapsed:: true
				- environment:: 
				  static-hosts:: 
				  dynamic-ip-range::
		- 10.0.10.192/26
			- 10.0.10.192/27
			  collapsed:: true
				- environment:: 
				  static-hosts:: 
				  dynamic-ip-range::
			- 10.0.10.224/27
			  collapsed:: true
				- environment:: [[Storage]] 
				  static-hosts:: [[NAS]] 
				  dynamic-ip-range:: N/A