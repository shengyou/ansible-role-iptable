
Install iptables [![Build Status](https://travis-ci.org/shengyou/ansible-role-iptable.svg?branch=master)](https://travis-ci.org/shengyou/ansible-role-iptable)
=========

安裝 iptables 並設置自訂的 rules。

* Ubuntu 14.04, 16.04
* CentOS 6, 7

Requirements
------------

* ansible >= 2.4
* python >= 2.6

Role Variables
--------------

以下 Variables 為必填項目，請指定防火牆 rules 的檔案位置。

使用方式請參考範例。

* custom_iptables_rules
* custom_ip6tables_rules


Dependencies
------------

none.

Example Playbook
----------------

```
- name: install_iptables.yml
  hosts: your_host
  gather_facts: yes
  become: yes

  vars:
   - custom_iptables_rules: /path/to/iptables_rules_filename.conf
   - custom_ip6tables_rules: /path/to/ip6tables_rules_filename.conf

  roles:
    - ansible-role-iptables
```

License
-------

MIT
