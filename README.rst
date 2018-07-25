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
* Password manager: pass_

The shell is configured based on the Prezto_ configuration framework. Whenever
possible, the gruvbox_ dark color scheme and the Hack_ font are used. The
Adwaita theme and the DejaVu Sans font are used for GTK+ applications.

Prerequisites
-------------

I recommend the installation of the latest Ansible version inside its own
virtual Python environment via the virtualenvwrapper_ script::

    sudo aptitude install virtualenvwrapper
    source /usr/share/virtualenvwrapper/virtualenvwrapper.sh
    mkvirtualenv --python=/usr/bin/python3 -i ansible py3-ansible

Note that ``aptitude`` is not installed by default, either install it
via ``apt-get`` or simply use ``apt-get`` directly.

Installation
------------

Here, I exemplary show how I install the desktop environment in my virtual
machine starting from a freshly installed minimal Ubuntu 18.04. From inside
the ``py3-ansible`` environment, the entire desktop is installed and configured
via::

    git clone https://github.com/kkrings/i3-ubuntu.git
    ansible-playbook -i i3-ubuntu/hosts --ask-become-pass --vault-id @prompt i3-ubuntu/kai-ubuntu-vm.yml

After a reboot, you should end up in a graphical LightDM session.

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

.. _pass:
    https://www.passwordstore.org/

.. _Prezto:
    https://github.com/sorin-ionescu/prezto/

.. _gruvbox:
    https://github.com/morhetz/gruvbox/

.. _Hack:
    https://sourcefoundry.org/hack/

.. _virtualenvwrapper:
    http://virtualenvwrapper.readthedocs.io/en/latest/
