======================
cookiecutter-openstack
======================

Cookiecutter template for an OpenStack project. See https://github.com/audreyr/cookiecutter.

* Free software: Apache license
* pbr_: Set up to use Python Build Reasonableness
* hacking_: Enforces the OpenStack Hacking Guidelines
* stestr_: Runs tests using stestr
* OpenStack-Infra_: Ready for OpenStack Continuous Integration testing
* Tox_ testing: Setup to easily test for Python 2.7, 3.5
* Sphinx_ docs: Documentation ready for generation and publication

Usage
-----

Install cookiecutter::

    pip install cookiecutter

Generate a Python package project::

    cookiecutter https://git.openstack.org/openstack-dev/cookiecutter.git

OpenStack projects require a working git repo for pbr to work, on newer
versions of cookiecutter (>= 0.7.0 released 2013-11-09) this initial commit will
be done automatically. Otherwise you will need to init a repo and commit to it
before doing anything else::

    cd $repo_name
    git init
    git add .
    git commit -a

Then:

* Add the project to the OpenStack Infrastructure


.. _pbr: https://docs.openstack.org/pbr/latest/
.. _OpenStack-Infra: http://docs.openstack.org/infra/system-config
.. _stestr: https://stestr.readthedocs.io/
.. _Tox: https://tox.readthedocs.io/en/latest/
.. _Sphinx: http://www.sphinx-doc.org/en/master/
.. _hacking: https://git.openstack.org/cgit/openstack-dev/hacking/plain/HACKING.rst
