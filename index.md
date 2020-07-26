# Formación Virtual
## Ciclo de Formación virtual

{%- extends "!layout.html" %}

{#

This template exists as a way to implement a version menu without changing what
the theme normally renders the menu on local builds and on builds on Read the
Docs. This is for local testing purposes only.

#}

{% block footer %}
  {% if not READTHEDOCS %}
    <div class="rst-versions" data-toggle="rst-versions" role="note" aria-label="versions">
      <span class="rst-current-version" data-toggle="rst-current-version">
        <span class="fa fa-book"> Read the Docs</span>
        v: latest
        <span class="fa fa-caret-down"></span>
      </span>
      <div class="rst-other-versions">
        <dl>
          <dt>{{ _('Versions') }}</dt>
          {% if test_versions %}
            {% for version in test_versions %}
            <dd><a href="#">{{ version }}</a></dd>
            {% endfor %}
          {% else %}
            <dd><a href="#">latest</a></dd>
            <dd><a href="#">1.0</a></dd>
            <dd><a href="#">1.1</a></dd>
          {% endif %}
        </dl>
        <dl>
          <dt>{{ _('Downloads') }}</dt>
          <dd><a href="#">PDF</a></dd>
          <dd><a href="#">ePub</a></dd>
          <dd><a href="#">HTML</a></dd>
        </dl>
        <dl>
          {# Translators: The phrase "Read the Docs" is not translated #}
          <dt>{{ _('On Read the Docs') }}</dt>
            <dd>
              <a href="#">{{ _('Project Home') }}</a>
            </dd>
            <dd>
              <a href="#">{{ _('Builds') }}</a>
            </dd>
        </dl>
        <dl>
          <dt>Debug</dt>
          <dd><a href="#" data-toggle="rst-debug-badge">Swap badge position</a></dd>
        </dl>
      </div>
    </div>
  {% endif %}
{% endblock %}

I'm glad you are here. I plan to talk about ...

1. Exploration of

section:
  - page: Introduction
    url: /contexto
    subsection:
      - page: Getting Started
        url: https://github.com/SIB-Colombia/Formacion/blob/master/contexto.md
      - page: Configuration
        url: /intro/config
      - page: Deploying
        url: /intro/deploy
  - page: Advanced Usage
    url: /usage
    subsection:
      - page: Customizing
        url: /usage/customizing
      - page: All Configuration Settings
        url: /usage/settings
      - page: Help and Support
        url: /usage/support
