{%- macro set_header_markup(header_text_length) -%}
{%- set servicelength = cookiecutter.service|length -%}
{%- for _ in range(0, servicelength + header_text_length) -%}={%- endfor -%}
{%- endmacro -%}
{%- macro set_header(header_text) -%}
{{ set_header_markup(header_text|length) }}
{{cookiecutter.service}}{{header_text}}
{{ set_header_markup(header_text|length) }}
{%- endmacro -%}
{{ set_header(" service overview") }}
The {{cookiecutter.service}} service provides...

The {{cookiecutter.service}} service consists of the following components:

``{{cookiecutter.module_name}}-api`` service
  Accepts and responds to end user compute API calls...
