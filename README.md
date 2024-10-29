Ansible rabbitmq
=========

Role for install rabbitmq and configure cluster.

Requirements
------------

Installed docker

Role Variables
--------------

All variables you can see in defaults.

For run cluster you need to run playbook with limit all nodes.

Set variable `rabbitmq_cluster_node` if need to start node in cluster.

`rabbitmq_resolve_peers` - list of extra hosts.

Example:
```yaml
rabbitmq_resolve_peers:
  - rabbit1:192.168.56.11
  - rabbit2:192.168.56.12
```

If you need to change container hostname, use variable `rabbitmq_hostname`.

Example Playbook
----------------

run-rabbitmq.yml
```yaml
- hosts: rabbitmq_hosts
  become: yes
  roles:
      - ageres210784.rabbitmq
```

License
-------

Apache 2.0

Author Information
------------------

[Evseev Sergey](https://github.com/Ageres210784)
