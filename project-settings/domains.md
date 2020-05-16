---
layout: default
title: Domains
nav_order: 1
parent: Project Settings
---

# Domains
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Default Domain

Every project has a default domain. Your website will be published under this default domain.
We use this domain to create links in emails and on your site.

For ease of use we add a domain like `your-perfect-project.hello-one.app` to your project.
You can use this domain as your primary domain, but we strongly recommend setting up a
[custom domain](#add-a-custom-domain) for your project.


## Add a Custom Domain
You can connect your site to any Domain you own.
On the domain settings page enter you domain name and click the "Add Domain" button.
Do this for every domain.

### Add `www.example.com` as a default domain
{: .no_toc }
Let's say you want to use `www.example.com` for your site. We recommend to also add the root domain
`example.com` to your project. Your site will then also be reachable under both domains.


Please note: We redirect all requests to the default domain. This prevents duplicate content.
{: .code-example }


### DNS Records

The connection with your domain is made with `CNAME` or `ANAME/ALIAS` DNS Records.
Therefore you must have access to your nameserver and be able to set DNS records. If you are not sure where to set DNS records please contact
your domain administrator or reach out to our support team.

For every domain you will receive a DNS CNAME or ALIAS Record.
Please add this record to your nameserver.

As soon as we have found the record and the record is valid your domain is conncted with your site.
In the background we will also issue a SSL certificate for your site.

Please note: it might take up to 24 hours until your domain is fully connected and a certificate has been issued.
{: .code-example }

### Managing TLS / SSL
All sites on hello one are served via SSL/TLS. It is not possible to disable SSL on your project.

If you need to disable TLS v1.x please submit a ticket to our support team.
If you want to use your own certificate please contact our support team.
