Downloads
#########

:sort: 1
:save-as: downloads.html

You can get bpython by downloading the latest release, cloning the git repo or 
using your system's package manager.

bpython has the following dependencies:

* Pygments

Release tarball
===============
The latest release for bpython is 0.13.1 and you can download it on our
`release page`_. You can find older releases here.

Git repository
==============
The development version is available with git; use the following command:

.. code-block:: shell

  git clone https://github.com/bpython/bpython/

If you get stuck, join #bpython on irc.freenode.net or send an email to the
mailing list (more info).

easy_install/pip
================
If you have ``easy_install`` or ``pip`` on your system (and you probably have)
you can install bpython through PyPi.

.. code-block:: shell

  easy_install bpython

or

.. code-block:: shell

  pip install bpython

Packages
========
(Note that packages may be out of date so please try at least the latest release if you have any problems before reporting bugs).

Debian
------
David Paleino maintains the bpython package. The package is included since
the release of squeeze. You can install it with:

.. code-block:: shell

  apt-get install bpython

Fedora
------
Terje Rosten has informed me that bpython is now in fedora, so "yum install bpython" should be all you need.

Ubuntu
------
The bpython package is included in the Ubuntu repositories starting at Ubuntu
9.10 Karmic Koala.You can install it with:

.. code-block:: shell

  apt-get install bpython

OpenSUSE
--------
This is an old version, please consider installing from tarball.

Pascal Bleser has been kind enough to provide a package for OpenSUSE, which can be found here:

http://download.opensuse.org/repositories/devel:/languages:/python/openSUSE_10.3/x86_64/bpython-0.2.3-1.1.x86_64.rpm

Apparently you can also add this repo:

http://download.opensuse.org/repositories/devel:/languages:/python/
to your package manager, if someone would like to submit the exact instructions for that, feel free.

Solaris
-------
You can find bpython packages for Solaris on the sunfreeware website, kindly provided for by Steven Christensen.

.. _release page: /releases/
