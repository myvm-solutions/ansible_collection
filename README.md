# ansible_collection
MyVM.Solutions common Ansible collection

## Modules:

- create_service
    - binary_path: string
    - binary_source: string
    - data_path: string
    - config_path: string
    - user: string

## Common dependencies

https://docs.ansible.com/ansible/latest/collections/ansible/builtin/user_module.html
- ansible.builtin.user
    - name
    - comment
    - create_home
    - shell
    - system
    - seuser

https://docs.ansible.com/ansible/latest/collections/ansible/builtin/systemd_service_module.html
- ansible.builtin.systemd_service module