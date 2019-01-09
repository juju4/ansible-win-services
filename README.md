[![Build Status - Master](https://travis-ci.org/juju4/ansible-win-services.svg?branch=master)](https://travis-ci.org/juju4/ansible-win-services)
[![Build Status - Devel](https://travis-ci.org/juju4/ansible-win-services.svg?branch=devel)](https://travis-ci.org/juju4/ansible-win-services/branches)(Syntax Only)

[![Appveyor - Master](https://ci.appveyor.com/api/projects/status/q5xmo6e1ijns8t05?svg=true)](https://ci.appveyor.com/project/juju4/ansible-win-services)
![Appveyor - Devel](https://ci.appveyor.com/api/projects/status/q5xmo6e1ijns8t05/branch/devel?svg=true)

# Windows services ansible role

Ansible role to setup services on Windows system.

## Requirements & Dependencies

### Ansible
It was tested on the following versions:
 * 2.3
 * 2.4
 * 2.5b2

### Operating systems

Tested in Appveyor

## Example Playbook

Just include this role in your list.
For example

```
- host: all
  roles:
    - juju4.win-services
```

Run
```
$ ansible -i inventory -m win_ping win --ask-pass
$ ansible-playbook -i inventory --limit win site.yml
```

## Variables

See defaults/main.yml for full scope

## Continuous integration

This role has a travis basic test (for github, syntax check only), Appveyor test and a Vagrantfile (test/vagrant).

```
$ cd /path/to/roles/juju4.win-services/test/vagrant
$ vagrant up
$ vagrant provision
$ vagrant destroy
$ ansible -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory -m win_ping -e ansible_winrm_server_cert_validation=ignore -e ansible_ssh_port=55986 all
```

## Troubleshooting & Known issues

## FAQ

Reference links
* http://www.marksanborn.net/howto/turn-off-unnecessary-windows-services/
* http://www.7tutorials.com/which-windows-services-are-safe-disable-when
* http://www.blackviper.com/service-configurations/black-vipers-windows-10-service-configurations/
* https://blogs.technet.microsoft.com/secguide/2017/05/29/guidance-on-disabling-system-services-on-windows-server-2016-with-desktop-experience/

## License

BSD 2-clause

