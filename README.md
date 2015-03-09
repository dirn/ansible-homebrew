Homebrew
========

An Ansible role to install and update Homebrew.

Requirements
------------

Only Ansible is required.

Role Variables
--------------

Several variables are available to configure the role.

To control where Homebrew's installer will live:

    homebrew_installer_root: ~

To install which libraries will be installed by Homebrew:

    homebrew_libraries: []

To keep Homebrew up-to-date:

    homebrew_update: true

To keep all of the libraries installed by Homebrew up-to-date:

    homebrew_upgrade_all: true

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: dirn.homebrew
          homebrew_installer_root: ~/.homebrew_installer
          homebrew_libraries:
            - git
            - vim
            - zsh
          homebrew_update: true
          homebrew_upgrade_all: false

License
-------

MIT

Author Information
------------------

This role was created by [Andy Dirnberger](https://github.com/dirn).
