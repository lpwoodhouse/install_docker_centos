# Ansible Play: install_docker_centos

### <sub-heading>

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

MIT

## Author Information

This role was created in 2022 by [Lee Woodhouse](https://www.leewoodhouse.com/)
