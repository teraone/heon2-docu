---
layout: default
title: E-Mail Sender Address
nav_order: 1
parent: Project Settings
---

# E-Mail Sender Address
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Concept
You will most likely send emails with our service.



## E-Mail From Name
You should use a short, precise and user friendly name. It will appear as a sender name in the email client.
Do not use long names or anything that might look spammy. A good example is `Java Developer Conference 2021`

## Reply to Address
If a user wants to reply to our emails we will send the answer to this email address.
```
    We do not parse incoming emails
```

## From Email Address
By default emails are sent from `no-reply@hello-one.app`.
While this might work for some customers we strongly recommend to setup a custom sender domain.



## Custom Sender Address
To add a custom sender address, you need access to your nameserver and be able to add some DNS records.
If you are not sure on how to set up DNS records please contact your domain administrator our our support team.


Before we can use your custom email address, we need to proof the ownership of it's domain.
Otherwise your emails will end up in spam folders or never even reach your customers.

### Step 1 Add your address
Click the "Use custom address" button and enter the desired email address.
You can only add domains you own.

This email domain can be the same as your [project domain](/project-settings/domains). But you can choose any domain or subdomain you own.

### Step 2 Add the DNS Records to your nameserver

After you have added the email address you will see a list of DNS Records.
Add these records to your domain.

### Step 3 Verify DNS Records
Click on "Refresh Status" and see if all records have been found or if there are errors.

```
It might take up to 24 hours until all records are verified. Usually it takes about 2 minutes.

```
As soon as all records are verified we will use your custom sender address for all emails
