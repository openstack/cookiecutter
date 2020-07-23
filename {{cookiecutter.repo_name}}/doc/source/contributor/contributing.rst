============================
So You Want to Contribute...
============================

For general information on contributing to OpenStack, please check out the
`contributor guide <https://docs.openstack.org/contributors/>`_ to get started.
It covers all the basics that are common to all OpenStack projects: the accounts
you need, the basics of interacting with our Gerrit review system, how we
communicate as a community, etc.

Below will cover the more project specific information you need to get started
with {{cookiecutter.service}}.

Communication
~~~~~~~~~~~~~
.. This would be a good place to put the channel you chat in as a project; when/
   where your meeting is, the tags you prepend to your ML threads, etc.

Contacting the Core Team
~~~~~~~~~~~~~~~~~~~~~~~~
.. This section should list the core team, their irc nicks, emails, timezones
   etc. If all this info is maintained elsewhere (i.e. a wiki), you can link to
   that instead of enumerating everyone here.

New Feature Planning
~~~~~~~~~~~~~~~~~~~~
.. This section is for talking about the process to get a new feature in. Some
   projects use blueprints, some want specs, some want both! Some projects
   stick to a strict schedule when selecting what new features will be reviewed
   for a release.

Task Tracking
~~~~~~~~~~~~~
.. This section is about where you track tasks- launchpad? storyboard? is there
   more than one launchpad project? what's the name of the project group in
   storyboard?

We track our tasks in {{ cookiecutter.bug_tracker }}
{% if cookiecutter.bug_tracker == 'Launchpad' %}
   https://bugs.launchpad.net/{{ cookiecutter.bug_project }}
{% elif cookiecutter.bug_tracker == 'Storyboard' %}
   https://storyboard.openstack.org/#!/project/{{ cookiecutter.bug_project }}
{% endif %}
If you're looking for some smaller, easier work item to pick up and get started
on, search for the 'low-hanging-fruit' tag.

.. NOTE: If your tag is not 'low-hanging-fruit' please change the text above.

Reporting a Bug
~~~~~~~~~~~~~~~
.. Pretty self explanatory section, link directly to where people should report
   bugs for your project.

You found an issue and want to make sure we are aware of it? You can do so on
{% if cookiecutter.bug_tracker == 'Launchpad' -%}
`Launchpad
<https://bugs.launchpad.net/{{ cookiecutter.bug_project }}>`_.
{%- elif cookiecutter.bug_tracker == 'Storyboard' -%}
`Storyboard
<https://storyboard.openstack.org/#!/project/{{ cookiecutter.bug_project }}>`_.
{%- endif %}

Getting Your Patch Merged
~~~~~~~~~~~~~~~~~~~~~~~~~
.. This section should have info about what it takes to get something merged. Do
   you require one or two +2's before +W? Do some of your repos require unit
   test changes with all patches? etc.

Project Team Lead Duties
~~~~~~~~~~~~~~~~~~~~~~~~
.. this section is where you can put PTL specific duties not already listed in
   the common PTL guide (linked below), or if you already have them written
   up elsewhere you can link to that doc here.

All common PTL duties are enumerated in the `PTL guide
<https://docs.openstack.org/project-team-guide/ptl.html>`_.
