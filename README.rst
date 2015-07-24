=============
bootstrap_env
=============

Problem
-------

There are many setups / strategies for how python dev environments' handle
`virtualenv`_. How can you create a bootstrapper for a team / open source
project that works across systems / opinions?

``bootstrap_env`` attempts to abstract this so you can create and source
across any POSIX-compliant shell with at least `virtualenv`_ installed.

Features
--------

- MIT licensed
- POSIX-compliant sh
- Portable
- Automatically detect if sourced
- Automatically detect the following virtualenv strategies:
  
  - `virtualenv`_
  - `virtualenvwrapper`_
  - `pyenv-virtualenv`_
  - `pyenv-virtualenvwrapper`_
    
Installation
------------

Assuming you have ``$HOME/.local/bin`` in your ``PATH`` (`need help w/ PATH?`_):

One-liner
~~~~~~~~~

.. code-block:: sh

    [ -d ~/.bootstrap_env ] || git clone https://github.com/tony/bootstrap_env.git ~/.bootstrap_env && [ -d ~/.local/bin ] || mkdir -p ~/.local/bin && ln -sf ~/.bootstrap_env/bootstrap_env.sh ~/.local/bin/bootstrap_env && rehash

Manual
~~~~~~

.. code-block:: sh
   
    $ cd ~/.local/bin
    
    # download w/ curl
    $ curl -o bootstrap_env.sh https://raw.githubusercontent.com/tony/bootstrap_env/master/bootstrap_env.sh
    
    # download w/ wget
    $ wget -o bootstrap_env.sh https://raw.githubusercontent.com/tony/bootstrap_env/master/bootstrap_env.sh
    
    # download w/ fetch (FreeBSD)
    $ fetch -o bootstrap_env.sh https://raw.githubusercontent.com/tony/bootstrap_env/master/bootstrap_env.sh
    
    # make executable
    $ chmod +x bootstrap_env.sh

.. _need help w/ PATH?: http://unix.stackexchange.com/q/131310
.. _virtualenv: https://virtualenv.pypa.io/en/latest/
.. _virtualenvwrapper: https://virtualenvwrapper.readthedocs.org/en/latest/
.. _pyenv-virtualenv: https://github.com/yyuu/pyenv-virtualenv
.. _pyenv-virtualenvwrapper: https://github.com/yyuu/pyenv-virtualenvwrapper
