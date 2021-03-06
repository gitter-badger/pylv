
pylv - run Python scripts in local virtual environment
======================================================

If you use venv or virtualenv for your Python project,
then you want of course to execute all Python scripts using the Python
executable from that venv/virtualenv (`venv/bin/python`) and
not the system one (`/usr/bin/python`).

This can be solved by using the shebang `#!/usr/bin/env pylv` instead of `#!/usr/bin/env python`.
The `pylv` script looks for `venv/bin/python` in current directory, then in parent directory etc.
and executes it.
So you can just run `./myscript.py` instead of `venv/bin/python myscript.py` or instead of
activating the virtual environment first.

It's less typing and much easier for non-developers (or non-Python developers).
