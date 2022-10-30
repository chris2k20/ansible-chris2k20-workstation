Ansible-Role: Generic Linux Workstation Config
=========

A simple ansile role to keep all your Linux Desktops in sync and make updates of packages very easy.

Requirements
------------

A normal ansible setup, where you place this repo in the `roles/workstation` folder.

Role Variables
--------------

Configure your workstation in the [defaults](./defaults/main.yml) or the ansible common way (host_vars, group_vars etc.).

Dependencies
------------

None.

Example Quickstart
------------------

If you are very lucky download that role via your ansible-galaxy into our `/usr/share/ansible/roles` and run ansible (no playbook or ansible structure needed): 

    # download that role from github
	ansible-galaxy role install  git+https://github.com/chris2k20/ansible-chris2k20-workstation -p /usr/share/ansible/roles --ignore-errors --force
        
    # run the role without a playbook
	ansible localhost -m include_role -a "name=ansible-chris2k20-workstation"

Example Playbook
----------------

Just run the role with your clients.

    - hosts: desktops
      roles:
         - { role: chris2k20.ansible-chris2k20-workstation, x: 42 }

License
-------

BSD

Author Information
------------------

chris2k20
