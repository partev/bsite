Known issues and FAQ
####################

:sort: 8
:save-as: issues.rst

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


.. _issue: https://github.com/bpython/bpython/issues
.. _issue: https://github.com/bpython/bpython/issues/494
