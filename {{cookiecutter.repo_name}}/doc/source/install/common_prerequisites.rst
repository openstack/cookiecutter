Prerequisites
-------------

Before you install and configure the {{cookiecutter.service}} service,
you must create a database, service credentials, and API endpoints.

#. To create the database, complete these steps:

   * Use the database access client to connect to the database
     server as the ``root`` user:

     .. code-block:: console

        $ mysql -u root -p

   * Create the ``{{cookiecutter.module_name}}`` database:

     .. code-block:: none

        CREATE DATABASE {{cookiecutter.module_name}};

   * Grant proper access to the ``{{cookiecutter.module_name}}`` database:

     .. code-block:: none

        GRANT ALL PRIVILEGES ON {{cookiecutter.module_name}}.* TO '{{cookiecutter.module_name}}'@'localhost' \
          IDENTIFIED BY '{{cookiecutter.module_name|upper}}_DBPASS';
        GRANT ALL PRIVILEGES ON {{cookiecutter.module_name}}.* TO '{{cookiecutter.module_name}}'@'%' \
          IDENTIFIED BY '{{cookiecutter.module_name|upper}}_DBPASS';

     Replace ``{{cookiecutter.module_name|upper}}_DBPASS`` with a suitable password.

   * Exit the database access client.

     .. code-block:: none

        exit;

#. Source the ``admin`` credentials to gain access to
   admin-only CLI commands:

   .. code-block:: console

      $ . admin-openrc

#. To create the service credentials, complete these steps:

   * Create the ``{{cookiecutter.module_name}}`` user:

     .. code-block:: console

        $ openstack user create --domain default --password-prompt {{cookiecutter.module_name}}

   * Add the ``admin`` role to the ``{{cookiecutter.module_name}}`` user:

     .. code-block:: console

        $ openstack role add --project service --user {{cookiecutter.module_name}} admin

   * Create the {{cookiecutter.module_name}} service entities:

     .. code-block:: console

        $ openstack service create --name {{cookiecutter.module_name}} --description "{{cookiecutter.service}}" {{cookiecutter.service|lower}}

#. Create the {{cookiecutter.service}} service API endpoints:

   .. code-block:: console

      $ openstack endpoint create --region RegionOne \
        {{cookiecutter.service|lower}} public http://controller:XXXX/vY/%\(tenant_id\)s
      $ openstack endpoint create --region RegionOne \
        {{cookiecutter.service|lower}} internal http://controller:XXXX/vY/%\(tenant_id\)s
      $ openstack endpoint create --region RegionOne \
        {{cookiecutter.service|lower}} admin http://controller:XXXX/vY/%\(tenant_id\)s
