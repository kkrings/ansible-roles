i3-ubuntu
=========

This repository contains a collection of Ansible_ roles for configuring my
personal Ubuntu virtual machine. Starting point is a Ubuntu 18.04 `minimal iso
image`_. A custom desktop environment is installed:

* Window manager: i3_
* Display manager: LigthDM
* Terminal emulator: LXTerminal
* Shell: Zsh
* Editor: Neovim_
* Web browser: Chromium_
* Document viewer: zathura_

The shell is configured based on the Prezto_ configuration framework. Whenever
possible, the gruvbox_ dark color scheme and the Hack_ font are used. The
Adwaita theme and the DejaVu Sans font are used for GTK+ applications.

Prerequisites
-------------

I recommend the installation of Ansible inside its own virtual Python
environment::

    mkvirtualenv --python=/usr/bin/python3 -i ansible py3-ansible

.. External links
.. _Ansible:
    https://www.ansible.com/

.. _minimal iso image:
    https://help.ubuntu.com/community/Installation/MinimalCD/

.. _i3:
    https://i3wm.org/

.. _Chromium:
    https://www.chromium.org/Home/

.. _zathura:
    https://pwmt.org/projects/zathura/

.. _Neovim:
    https://neovim.io/

.. _Prezto:
    https://github.com/sorin-ionescu/prezto/

.. _gruvbox:
    https://github.com/morhetz/gruvbox/

.. _Hack:
    https://sourcefoundry.org/hack/
