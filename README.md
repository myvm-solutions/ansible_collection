# ansible_collection
MyVM.Solutions common Ansible collection

## Prerequisites:

`ansible-galaxy collection install prometheus.prometheus`

```bash
cd ansible_collection
ln -s $(pwd)/myvm $HOME/.ansible/collections/ansible_collections/
```

## Roles:

### Create systemd service

Development placed on hold, current need satisfied by `prometheus.prometheus` package.

```yaml
- manage_systemd_service:
    action: add
    binary_path: string
    binary_source: string
    data_path: string
    config_path: string
    user: string
    enabled: bool
    started: bool
```

### Install prometheus server

Calls `prometheus.prometheus.prometheus` with some defaults.
https://prometheus-community.github.io/ansible/branch/main/prometheus_role.html

### Install prometheus node_exporter

Calls `prometheus.prometheus.node_exporter` with some defaults.
https://prometheus-community.github.io/ansible/branch/main/node_exporter_role.html

## Common dependencies

https://docs.ansible.com/ansible/latest/collections/ansible/builtin/user_module.html
```yaml
- ansible.builtin.user:
    name: string
    comment: string
    create_home: string
    shell: string
    system: string
    seuser: string
```

https://docs.ansible.com/ansible/latest/collections/ansible/builtin/systemd_service_module.html
```yaml
- ansible.builtin.systemd_service module
```
