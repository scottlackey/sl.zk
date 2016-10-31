## Ansible role for installing and configuring Zookeeper clusters
Installs [zookeeper](http://zookeeper.apache.org/)

## Example Playbook
    hosts: zk
    roles:
      - sl.zk

## example group_vars required values
     zookeeper_hosts: 'zk-0.example.com:2181,zk-1.example.com:2181'


##Optional
- log_level - Log level to be used for zookeeper logs. Defaults to WARN
- zookeeper_id - Id to be used if one can't or shouldn't be derived from zookeeper_hosts. This will happen if zookeeper_hosts doesn't contain the fqdn but an alias
- zookeeper_heap_opt - Java Heap option for the zookeeper process. Default is to let the JRE decide

