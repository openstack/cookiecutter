2. Edit the ``/etc/{{cookiecutter.module_name}}/{{cookiecutter.module_name}}.conf`` file and complete the following
   actions:

   * In the ``[database]`` section, configure database access:

     .. code-block:: ini

        [database]
        ...
        connection = mysql+pymysql://{{cookiecutter.module_name}}:{{cookiecutter.module_name|upper}}_DBPASS@controller/{{cookiecutter.module_name}}
