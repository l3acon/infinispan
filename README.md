# Ansible Collection - l3acon.infinispan

Documentation for the collection.

## Using me
### Get this collection
```bash
$ ansible-galaxy install l3acon.infinispan
```

Have a `site.yml` that sets some variables.

```yaml
- name: Deploy infinispan
  hosts: all
  become: true
  tasks:
    - name: include role
      include_role: 
        name: l3acon.infinispan.infinispan
      vars:
        infinispan_bind_addr: site-local
        infinispan_users: 
          - name: myadminuser
            password: myadminpassword
            roles: supervisor
```
