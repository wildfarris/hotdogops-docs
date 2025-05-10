## Firewall
	- external-connectivity:: [[Spectrum]] (Tier 1), [[Verizon]] (Tier 2)
	  virtual-ips:: 10.0.10.27, 10.0.10.200, 10.0.10.210, 10.0.10.28 
	  internal-subnets:: [Home]([[Home Network]]), [Lab]([[Lab Network]])
	  hosted-services:: [[DNS Resolver]], [[DHCP]], [[HAProxy]]
- ## NAS
	- hosted-services:: [[PBS]], [[QuObjects]], [[NFS]]
- ## Virtualization
	- cluster:: {{embed [[labpharesio]]}}
- ## Kubernetes Clusters
	- {{embed [[Prod]]}}
	- {{embed [[Dev]]}}
	- {{embed [[Sandbox]]}}