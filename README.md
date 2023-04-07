# Ansible role to install a Prometheus with podman on RHEL based systems

## Example playbook

```yaml

# run: ansible-playbook -i ./inv/${CLUSTER} /hosts ./pb_prometheus.yml --extra-vars="target=mon_hosts" -u root

---
- name: "Install podman with prometheus"
  hosts: '{{ target | default("noname.example.com") }}'
  gather_facts: false

  roles:
    - do.prometheus

```
