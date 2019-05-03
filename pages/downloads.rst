Downloads
#########

:sort: 1
:save-as: downloads.html

You can get bpython by downloading the latest release, cloning the git repo or
using your system's package manager.

bpython has the following dependencies:

* ``Pygments``
* ``requests``
* ``Sphinx`` != 1.1.2 (for the documentation only)
* ``mock`` (for the testsuite only)
* ``babel`` (optional, for internationalization)
* ``curtsies`` >= 0.1.18
* ``greenlet``
* ``urwid`` (for bpython-urwid only)

If you are using Python 2 before 2.7.7, the following dependency is also
required:

* ``requests[security]``

If you have problems installing ``cffi`` which is needed by ``pyOpenSSL``,
please take a look at ``cffi``'s `documentation`_.

Release tarball
===============
The latest release for bpython is **0.17.1** and you can download it on our
`release page`_. You can find older releases here.

Git repository
==============
The development version is available with git; use the following command:

.. code-block:: shell

  git clone https://github.com/bpython/bpython/

If you get stuck, join #bpython on irc.freenode.net or send an email to the
mailing list (more info).

pip/easy_install
================
If you have ``pip`` on your system (and you probably have)
you can install bpython through PyPi.

.. code-block:: shell

  pip install bpython

In case of you don't have ``pip``, you could use deprecated ``easy_install`` command:

.. code-block:: shell

  easy_install bpython


Packages
========
(Note that packages may be out of date so please try at least the latest release
if you have any problems before reporting bugs).

Debian
------
David Paleino maintains the bpython package. The package is included since
the release of squeeze. You can install it with:

.. code-block:: shell

  apt-get install bpython

Fedora
------
Terje Rosten has informed me that bpython is now in Fedora, so "yum install
bpython" should be all you need.

Ubuntu
------
The bpython package is included in the Ubuntu repositories starting at Ubuntu
9.10 Karmic Koala.You can install it with:

.. code-block:: shell

  apt-get install bpython

OpenSUSE
--------
Packages for OpenSUSE can be found at

https://software.opensuse.org/download.html?project=devel:languages:python&package=bpython

Please follow the instructions there to install bpython with `zypper`.

Solaris
-------
You can find bpython packages for Solaris on the sunfreeware website, kindly
provided for by Steven Christensen.

.. _documentation: https://cffi.readthedocs.org/en/release-0.8/#macos-x
.. _release page: /releases/

OpenBSD
-------
A bpython package is available in the OpenBSD repositories. You can install it with:

.. code-block:: shell

  pkg_add bpython
