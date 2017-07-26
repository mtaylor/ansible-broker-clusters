AMQ Cluster Playbook
=========

Deploys JBoss AMQ 7 Broker cluster.

Requirements
------------

Requirements are present on the requirements.yml file. To install them:

```ansible-galaxy install -f -r requirements.yml```

Playbook details
--------------

This project contains 3 playbooks:

* provision-host.yml: to prepare a RHEL, CentOS or Fedora system for being a broker host.
* provision-broker.yml: to install, configure and create clustered broker instances.
* provision.yml: to install a whole system from scratch (both the host and the broker).


Usage
--------------

Install everything:
```ansible-playbook provision.yml -v -u root -i ./inventory/development.yml```


Install the broker only:
```ansible-playbook provision-broker.yml -v -u root -i ./inventory/development.yml```