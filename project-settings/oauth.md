---
layout: default
title: OAuth Clients
nav_order: 7
parent: Project Settings
---

# OAuth Clients
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## General Concept
OAuth Clients can be used to allow your guests to login into third party applications using their login data from hello-one.

For example, you want your guests to be able to use their accounts for external applications. 

Our OAuth is following the [OAuth 2.0](https://tools.ietf.org/html/rfc6749) practices through [Laravel Passport](https://laravel.com/docs/8.x/passport).

## Add Client Applications

You add new OAuth clients by clicking the **Add Client** button above the OAuth Clients list.

Now you enter the name of the external application, the OAuth callback URL of said application, and you choose if you want your guests to reenter their login information before they're redirected to the external application.

After entering the information, you're receiving a Client ID and a Client Secret. Both values are required by your external application to communicate with our application.  
**Be careful! You won't be able to look them up later.**
