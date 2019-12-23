---
layout: default
title: Quick Start
nav_order: 1
parent: Theme Developer
---

# Quick Start

{: .no_toc }

Quick start guide for theme developers
{: .fs-6 .fw-300 }

## Table of contents

{: .no_toc .text-delta }

1. TOC
   {:toc}

---

## Create a Theme Folder

You’ll need a folder to store the contents of your theme.

```
$ mkdir theme-name
$ cd theme-name
```

## Folder Structur

Every theme consists at least of a `package.json` and a page template.

| name           | Description                               |
| :------------- | :---------------------------------------- |
| /pages/        | folder of page templates                  |
| /sections/     | folder of section templates               |
| /partials/     | folder of partial templates               |
| /emails/       | folder of email templates                 |
| /assets/       | assets of the theme (e.g. css & js files) |
| /packages.json | configuration file of the theme           |

## The Configuration File

Start by creating a `package.json` file in the root of your project and add some basic information.

```json
{
  "name": "@teraone/theme-name",
  "description": "example theme",
  "license": "MIT",
  "author": {
    "name": "unknown",
    "email": "pool@teraone.de",
    "url": "https://teraone.de"
  },
  "repository": {
    "type": "git",
    "url": "https://github.com/teraone/default-template"
  }
}
```

### Theme Configuration

{: .no_toc }
Settings and configuration of the theme are stored in the `config` object.

```json
{
  "config": {
    "defaultPageTemplate": "pages/default.twig"
  }
}
```

The configuration above specifies the path of the default page template, which should be used to render a page.

### Theme Settings

{: .no_toc }
If you want the user to be able to customize your theme by setting some variables, you can use the `themeSettings` array.

```json
{
  "config": {
    "themeSettings": [
      {
        "name": "textColor", // name of the setting
        "category": "colors", // used for categorisation
        "type": "select",
        "options": {
          "blue": "Blue Text",
          "green": "Green Text"
        }, // avaible options
        "value": "blue" // default value
      }
    ]
  }
}
```

The setting above enables the user to select the text color of the theme. The user is able to select one of the `options`. The default is `blue`.

## Template Files

Hello One uses [**twig**](https://twig.symfony.com/) for rendering any template files of a theme.

More Information:

[Twig Docs](https://twig.symfony.com/doc/2.x/templates.html){: .btn }.

A template is just a simple `.twig` file. If the user should be able to set some options you should also create a corresponding `.twig.json` file.

## Page Templates

Templates for rendering a page are located in the `/pages` folder.

Let's start by creating a simple page template.

/pages/default.twig

```html
<!-- {% block content %}
    <div>
        <h1>Page Template</h1>
    </div>
{% endblock content %} -->
```


## Template Options

If the user should be able to set some page specific settings, create an corresponding `.twig.json` file.

/pages/default.twig.json

```json
[
  {
    "name": "color",
    "type": "select",
    "value": "blue",
    "options": ["blue", "red", "green"]
  }
]
```

The above option enables the user to select a color for every page and sets the default to blue.

You can now use the variable in the template file

```html
<!-- {% block content %}
    <div style="background-color: {{ color }}">
        <h1>Page Template</h1>
    </div>
{% endblock content %} -->
```

## Section Templates

Templates for rendering a section are located in the `/sections` folder. In order to render the sections of a page, we will insert the follwing code in our page template.

/pages/default.twig

```html
    <!-- <div>
        <h1>Page Template</h1>

        {% block sections %}
            {% for section in page.sections %}
                {% include section._template_name with section.data %}
            {% endfor %}
        {% endblock %}

    </div> -->
```

## Using the Hello One Theme Editor

## Asset Folder

## Forms

## E-Mails

## Upload your Theme
