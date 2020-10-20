---
layout: default
title: Webhooks
nav_order: 6
parent: Project Settings
---

# Webhooks
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Webhooks

[Webhooks](https://en.wikipedia.org/wiki/Webhook) can be used to trigger events on any external server.
For example if a Guest registered on your site you can send his data to an invoicing service and send him a invoice.

All request are signed. You should always verify the signature of our requests. So you can be sure the request came from us

If a request fails, we attempt to send it again for 2 times.


## Add a webhook
Your endpoint URL must be secure (https only) and the certificate must be valid.
We do not follow redirects. We abort every request after 5 seconds.


## Verify the webhook signature


### Step 1: Extract the salt and signature from the header

We send two headers with every webhook request
```
  x-hello-one-signature: $SIGNATURE
  x-hello-one-signature-salt: $SALT
```

### Step 2: Prepare the `signed_payload` string

The `signed_payload` string is created by concatenating:
```
    The $SALT (as a string)
    The character .
    The actual JSON payload (i.e., the request body)
```

### Step 3: Determine the expected signature

Compute an HMAC with the SHA256 hash function. Use the endpoint’s `signing secret` as the key, and use the `signed_payload` string as the message.

### Step 4: Compare the signatures

Compare the signature in the header to the expected signature.

## Choosing Events
Please select only the events you want be informed about. So we won't hammer your servers.


## Request Logs
If you do not receive any webhook requests, have a look in the logs and you can see all sent requests and their errors.

