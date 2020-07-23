The source repository for this project can be found at:

   https://opendev.org/{{ cookiecutter.repo_group }}/{{ cookiecutter.repo_name }}

Pull requests submitted through GitHub are not monitored.

To start contributing to OpenStack, follow the steps in the contribution guide
to set up and use Gerrit:

   https://docs.openstack.org/contributors/code-and-documentation/quick-start.html

Bugs should be filed on {{ cookiecutter.bug_tracker }}:
{% if cookiecutter.bug_tracker == 'Launchpad' %}
   https://bugs.launchpad.net/{{ cookiecutter.bug_project }}
{% elif cookiecutter.bug_tracker == 'Storyboard' %}
   https://storyboard.openstack.org/#!/project/{{ cookiecutter.bug_project }}
{% endif %}
For more specific information about contributing to this repository, see the
{{ cookiecutter.service }} contributor guide:

   https://docs.openstack.org/{{ cookiecutter.repo_name }}/latest/contributor/contributing.html
