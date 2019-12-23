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

Start by creating a `package.json` file in the root of your project.
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
    "config": {
        "defaultPageTemplate": "pages\/default.twig",
        "themeSettings": [
            {
                "name": "useSidebar",
                "category": "menu",
                "type": "text",
                "value": "Hallo Welt"
            },
            {
                "name": "backgroundColor",
                "category": "colors",
                "type": "select",
                "options": {
                    "green": "green",
                    "blue": "blue"
                },
                "value": "green"
            },
            {
                "name": "textColor",
                "category": "colors",
                "type": "select",
                "options": {
                    "blue": "Blue Text",
                    "green": "Green Text"
                },
                "value": "blue"
            }
        ]
    },
    "repository": {
        "type": "git",
        "url": "https:\/\/github.com\/teraone\/default-template"
    }
}
```

## Page Templates



## Section Temaplates

## Asset Folder

## Forms

## E-Mails

## Upload your Theme
