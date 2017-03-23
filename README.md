openshift-cluster-groupsync
=========

An Ansible role for synchronizing groups across OpenShift clusters.

Installation
------------

```
ansible-galaxy install https://github.com/jkupferer/ansible-role-openshift-cluster-groupsync/archive/master.tar.gz#/openshift-cluster-groupsync
```

Requirements
------------

OpenShift clusters with service accounts with a tokens that can be used to
access both clusters.

Role Variables
--------------

* `src_cluster_url`

* `src_cluster_token`

* `dest_cluster_url`

* `dest_cluster_token`

Example Playbook
----------------

    - hosts: masters[0]
      roles:
      - role: openshift-cluster-groupsync
        src_cluster_url: https://master.cluster1.example.com
        src_cluster_token: eyJhbGciOiJSUzI1NiIsInR5cCI...
        dest_cluster_url: https://master.cluster2.example.com
        dest_cluster_token: hbeciOiyJGJSUzI1NiIcCIsInR5...

License
-------

BSD

Author Information
------------------

Johnathan Kupferer (jkupfere@redhat.com)
