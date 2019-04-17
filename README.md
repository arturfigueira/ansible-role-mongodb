# MongoDB
Ansible role to install and configure MongoDB on RHEL/CentOS 6

## Dependences
None.

## Variables
```yml
#MongoDB Version
mongodb_version: MongoDB Version to be Installed. Default: 3.4.1
mongodb_repo_gpgcheck: 0 to no check, 1 to check. Default: 0
mongodb_daemon: Service Name. Default: mongod
mongodb_port: MongoDB listenning port. Default: 27017
mongodb_conf_bind_ip: IP bind for Mongo service. Default: 127.0.0.1
```

## Playbook
```yml
- name: Install and Configure MongoDB
  hosts: all
  become: yes
  become_user: root
  roles:
    - role: mongodb
      vars:
        mongodb_conf_bind_ip: 0.0.0.0
        mongodb_port: 27099
```

## Compatibility

* [Ansible 2.+](https://www.ansible.com/)
* [CentOS 6 / 7](https://www.centos.org/)

## Contributing
Please read [CONTRIBUTING.md]([CONTRIBUTING.md]) for details on our code of conduct, and the process for submitting pull requests to me.

## Versioning
We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository]().

## Authors
*  [ArturFigueira](https://github.com/arturfigueira) - *Initial work*

## License
This project is licensed under the GNU GENERAL PUBLIC LICENSE - see the [LICENSE.md](LICENSE.md) file for details.
