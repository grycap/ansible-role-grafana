[![License](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)
[![Build Status](https://travis-ci.org/grycap/ansible-role-grafana.svg?branch=master)](https://travis-ci.org/grycap/ansible-role-grafana)

Grafana Role
===================

Install [Grafana](http://grafana.org/).  
This role has been tested only with Ubuntu 16. Is not ensured that it will work with other systems.

Role Variables
--------------

Variables used in this role:

	## Grafana
	grafana_datasource_git_repo: "https://github.com/openstack/monasca-grafana-datasource.git"
	grafana_datasource_git_branch: "master"
	grafana_git_repo: "https://github.com/twc-openstack/grafana.git"
	grafana_git_branch: "master-keystone"
	## Keystone
	keystone_ip_address: "127.0.0.1"
	## Go
	go_version: "1.8"
	## NodeJS
	node_js_version: "7.6.0"
	## NVM
	nvm_version: "0.33.1"
	## System info
	grafana_system_user_name: grafana
	grafana_system_group_name: grafana
	grafana_system_comment: Grafana system user
	grafana_system_shell: /bin/false
	grafana_system_user_home: "/var/lib/{{ grafana_system_user_name }}"

Example Playbook
----------------
```
- hosts: server
  roles:
  - { role: 'grycap.grafana' }
```

Contributing to the role
========================
In order to keep the code clean, pushing changes to the master branch has been disabled. If you want to contribute, you have to create a branch, upload your changes and then create a pull request.  
Thanks
