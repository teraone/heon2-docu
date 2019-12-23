---
layout: default
title: Quick Start
nav_order: 1
parent: Theme Developer
---

# Quick Start
{: .no_toc }


Quick start guide for Theme Developers
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

## The Configuration File

Start by creating a `package.json` file in the root of your project and add some basic information.
```json
{
    "name": "@teraone\/theme-name",
    "description": "example theme",
    "license": "MIT",
    "author": {
        "name": "unknown",
        "email": "pool@teraone.de",
        "url": "https:\/\/teraone.de"
    },
    "repository": {
        "type": "git",
        "url": "https:\/\/github.com\/teraone\/default-template"
    }
}
```

### Theme Configuration

Settings and configuration of the theme are stored in the `config` object.

```json
{
    "config": {
        "defaultPageTemplate": "pages\/default.twig",
    }
}
```
The configuration above specifies the path of the default page template, which should be used to render a page.


#### Theme Settings

If you want the user to be able to customize your theme by setting some variables. You can use the `themeSettings` array.
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

## Page Templates



## Section Temaplates

## Asset Folder

## Forms

## E-Mails

## Upload your Theme
