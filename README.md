# Ansible Playbook: install_docker_centos
![GitHub last commit](https://img.shields.io/github/last-commit/lpwoodhouse/playbook_install_docker_centos)
![GitHub repo file count](https://img.shields.io/github/directory-file-count/lpwoodhouse/playbook_install_docker_centos)
![GitHub top language](https://img.shields.io/github/languages/top/lpwoodhouse/playbook_install_docker_centos)

## Purpose

This play is for installing docker and portainer on a centos host.<br>

## Requirements

collections:<br>
  - community.docker

## Role Variables

Default role variables for the install_portainer role are listed below (see ```defaults/main.yml```)
```shell
centos_baseurl: https://download.docker.com/linux/centos/docker-ce.repo
docker_packages:
  - docker-ce
  - docker-ce-cli
  - containerd.io
  - docker-compose-plugin
docker_users:
  - ansible
```
Default role variables for the install_portainer role are listed below (see ```defaults/main.yml```)
```shell
dockerhub_user: <value>
dockerhub_pass: <value>
```
## Dependencies

None

## Example Playbook
```yaml
    - hosts: all
      become: true
      roles:
        - install_docker_centos
        - install_portainer
```

## License

[![GitHub](https://img.shields.io/github/license/lpwoodhouse/playbook_install_docker_centos)](LICENSE)

## Author Information

This playbook was created in 2022 by [Lee Woodhouse](https://www.leewoodhouse.com/)
