[![Build Status](https://travis-ci.org/bitintheskud/ansible-role-docker-ce-centos.svg?branch=master)](https://travis-ci.org/bitintheskud/ansible-role-docker-ce-centos)

# Ansible role to install Docker CE

Ansible role to install Docker CE on CentOS 7

## Requirements

None

## Role Variables

name | required | default | example | description
--- | --- | --- | --- | ---
docker_centos_users | no | [] | ["vagrant"] | Users added to docker group
docker_version | no | "" | "17.12.1" | Install a specific docker version. None will install the latest version.
docker_install_dir | no | "/var/docker/install" | "/tmp" | Download script in this directory


## Dependencies

 - Centos 7

## Example Playbook

```yaml

---
- hosts: localhost
  connection: local
  gather_facts: true
  become: yes

  vars:
     docker_centos_users:
       - vagrant

  environment: 
    VERSION: "{{ docker_version }}"

  roles:
    - ansible-role-docker-ce-centos
```
## What's next 

- Make it for debian and ubuntu. 
- Reinstall docker if not in target version. 

## License

[MIT](LICENSE)
