Role Name
=========
[![license][2i]][2p]
[![twitter][3i]][3p]

A role to install fish (2.2) and fisher

Description
-----------

Nothing too major. The role installs the shell [fish][4] with [fisher][5].
It is pretty barren for now except with those two options...

Role Variables
--------------

There are two variables:

``` yaml
user.home # the $HOME to have the shell be used in
user.name # the $USER for the shell to be used in
```

Requirements
------------

The role requires the [abaez.common][6] role to run properly. This is the only requirement with the variables that need to be changed.


Usage
-----

To use the role, you need to give become access for the user you want to have the shell be installed and configured for. You also need to add the [abaez.common][6] for the role to function. An example can be seen below:

``` yaml
- hosts: servers
    roles:
        - abaez.common
        - abaez.fish
```

Author Information
------------------

[Alejandro Baez][1]

[1]: https://keybase.io/baez
[2i]: https://img.shields.io/badge/license-BSD_2-green.svg
[2p]: ./LICENSE
[3i]: https://img.shields.io/badge/twitter-a_baez-blue.svg
[3p]: https://twitter.com/a_baez
[4]: http://fishshell.com/
[5]: https://github.com/fisherman/fisherman
[6]: https://galaxy.ansible.com/abaez/common
