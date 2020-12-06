ansible-role-k8s-certificates
=========

* Installs CFSSL and generates certificates for a Kubernetes cluser.
* Intended use is to run on an host to generate a folder with all necessary TLS certificates for a cluster.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

Required variables:
* k8s_api_lb_ip
The IP address of the load balancer to be used for the Kubernetes API, i.e. "192.168.1.50"

* k8s_cert_org_name
Org name for certificates, i.e. "Kubernetes The Hard Way"

* k8s_conf_files_dir
...

* local_id
...

These will default to the values on the current host. If you're running against a remote target, supply these variables.
k8s_cert_cfssl_os:
* linux, darwin, windows
k8s_cert_cfssl_arch:
* amd64, aaarch64, etc

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
