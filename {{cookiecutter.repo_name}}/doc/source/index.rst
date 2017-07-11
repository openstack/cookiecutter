{%- macro set_header_markup(header_text_length) -%}
{%- set module_name_length = cookiecutter.module_name|length -%}
{%- for _ in range(0, module_name_length + header_text_length) -%}={%- endfor -%}
{%- endmacro -%}
{%- macro set_header(header_text) -%}
{{ set_header_markup(header_text|length) }}
{{header_text}}{{cookiecutter.module_name}}
{{ set_header_markup(header_text|length) }}
{%- endmacro -%}

.. {{ cookiecutter.repo_name }} documentation master file, created by
   sphinx-quickstart on Tue Jul  9 22:26:36 2013.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

{{ set_header("Welcome to the documentation of ") }}

Contents:

.. toctree::
   :maxdepth: 2

   readme
   install/index
   library/index
   contributor/index
   configuration/index
   cli/index
   user/index
   admin/index
   reference/index

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
