===============================
{{ cookiecutter.repo_name }}
===============================

{{ cookiecutter.project_short_description}}

Please fill here a long description which must be at least 3 lines wrapped on
80 cols, so that distribution package maintainers can use it in their packages.
Note that this is a hard requirement.

* Free software: Apache license
* Documentation: https://docs.openstack.org/{{ cookiecutter.repo_name }}/latest
* Source: https://git.openstack.org/cgit/{{cookiecutter.repo_group}}/{{ cookiecutter.repo_name }}
{%- if cookiecutter.bug_tracker == 'Launchpad' -%}
* Bugs: https://bugs.launchpad.net/{{ cookiecutter.bug_project }}
{%- elif cookiecutter.bug_tracker == 'Storyboard' -%}
* Bugs: https://storyboard.openstack.org/#!/project/{{ cookiecutter.bug_project }}
{%- endif -%}

Features
--------

* TODO
