<!--
  templateType: page
  isAvailableForNewContent: true
  label: About
  screenshotPath: ../images/template-previews/about.png
-->
{% extends './layouts/base.html' %}

{% block body %}
{# The main-content ID is used for the navigation skipper in the header.html file. More information on the navigation skipper can be found here: https://github.com/HubSpot/cms-theme-boilerplate/wiki/Accessibility #}
<main id="main-content" class="body-container-wrapper">
  {% dnd_area 'dnd_area' class='body-container body-container--about', label='Main section' %}

    {# Main section #}
    {% dnd_section
      vertical_alignment='TOP'
    %}
      {% dnd_module path='@hubspot/linked_image',
        img={
          'alt': 'Coworkers sitting together and smiling outside.',
          'size_type': 'auto',
          'src': get_asset_url('../images/team-image.png')
        },
        offset=0,
        width=6
      %}
      {% end_dnd_module %}
      {% dnd_module path='@hubspot/rich_text',
        offset=6,
        width=6
      %}
        {% module_attribute 'html' %}
          <h1>Meet our team</h1>
          <p>Use this page to help your visitors learn more about you. Include images so that folks will recognize you at conferences and events.</p>
        {% end_module_attribute %}
      {% end_dnd_module %}
    {% end_dnd_section %}
    {# End main section #}

  {% end_dnd_area %}
</main>
{% endblock body %}
© 2021 GitHub, Inc.
