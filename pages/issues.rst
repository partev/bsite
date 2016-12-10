Known issues and FAQ
####################

:sort: 8
:save-as: issues.html

For a list of unfixed issues, please check our issue_ tracker.


No module named `configparser`
==============================

If launching `bpython` fails with

.. code-block:: pytb

    Traceback (most recent call last):
      File "/usr/local/bin/bpython", line 7, in <module>
        from bpython.curtsies import main
      File "/Library/Python/2.7/site-packages/bpython/curtsies.py", line 14, in <module>
        from bpython.curtsiesfrontend.repl import Repl
      File "/Library/Python/2.7/site-packages/bpython/curtsiesfrontend/repl.py", line 32, in <module>
        from bpython.config import (Struct, loadini, default_config_path,
      File "/Library/Python/2.7/site-packages/bpython/config.py", line 9, in <module>
        from six.moves.configparser import ConfigParser
    ImportError: No module named configparser

there is an old `six` (pre 1.5) version in `sys.path` that gets loaded instead
of the correct one. Make sure a new enough `six` version is placed in
`sys.path`.

This issue seems to be Mac OS X specific. In issue 494_ it was mentioned that
the following entry in `~/.bashrc` fixes the issue:

.. code-block:: shell

  export PYTHONPATH=/Library/Python/2.7/site-packages/:$PYTHONPATH


Upload failed: hostname 'bpaste.net' doesn't match either of '\*.qabana.nl', 'qabana.nl'
========================================================================================

This issues is caused by missing SNI support in Python respectively `requests`.
There are two possible fixes for this issue:

* Upgrade to Python 2.7.7 or newer.
* Make sure that `pyOpenSSL`, `pyasn1`, and `ndg-httpsclient` are installed.

pkg_resources.DistributionNotFound: ndg-httpsclient
===================================================

If launching `bpython` fails with

.. code-block:: pytb

    Traceback (most recent call last):
      File "/tmp/bpython-26/bin/bpython", line 5, in <module>
        from pkg_resources import load_entry_point
      File "/tmp/bpython-26/lib/python2.6/site-packages/pkg_resources.py", line 2829, in <module>
        working_set = WorkingSet._build_master()
      File "/tmp/bpython-26/lib/python2.6/site-packages/pkg_resources.py", line 449, in _build_master
        ws.require(__requires__)
      File "/tmp/bpython-26/lib/python2.6/site-packages/pkg_resources.py", line 742, in require
        needed = self.resolve(parse_requirements(requirements))
      File "/tmp/bpython-26/lib/python2.6/site-packages/pkg_resources.py", line 639, in resolve
        raise DistributionNotFound(req)
    pkg_resources.DistributionNotFound: ndg-httpsclient

after a successful install, something went wrong during the installation of the
dependencies (i.e. they were not correctly resolved). Installing the
`pyOpenSSL`, `pyasn1` and `ndg-httpsclient` manually should resolve this issue.

This issue has been observed with old Python (2.6.X) and pip versions and it
should not be present in newer versions.

Building `cffi` fails to build on Mac OS X
==========================================

If you have problems installing `cffi` which is needed by `pyOpenSSL`,
please take a look at `cffi`'s documentation_.


<F1> does not work in GNOME terminal
====================================

By default GNOME terminal does not forward <F1> to the application. This can be
fixed by `removing <gnometerminal>`_ the <F1> key binding in GNOME terminal.

.. _issue: https://github.com/bpython/bpython/issues
.. _494: https://github.com/bpython/bpython/issues/494
.. _documentation: https://cffi.readthedocs.org/en/release-0.8/#macos-x
.. _gnometerminal: http://askubuntu.com/questions/37313/how-do-i-deactivate-f1-and-f10-keybindings-in-gnome-terminal
