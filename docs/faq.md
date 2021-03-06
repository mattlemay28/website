---
layout: page
title: FAQ
permalink: /docs/faq/
top_graphic: 1
date: 2017-2-22T00:00
---

Last updated: {{ page.date | date: "%B %d, %Y" }} \| [See all Documentation](/docs/)

This FAQ is divided into the following sections:

* [General Questions](#general)
* [Technical Questions](#technical)

# <a name="general">General Questions</a>

## What services does Let's Encrypt offer?

Let's Encrypt is a global Certificate Authority (CA). We let people and organizations around the world obtain, renew, and manage SSL/TLS certificates. Our certificates can be used by websites to enable secure HTTPS connections.

Let’s Encrypt offers Domain Validation (DV) certificates. We do not offer Organization Validation (OV), Extended Validation (EV), or wildcard certificates, primarily because we cannot automate issuance for those types of certificates.

To get started using Let's Encrypt, please visit our [Getting Started](https://letsencrypt.org/getting-started/) page.

## What does it cost to use Let's Encrypt? Is it really free?

We do not charge a fee for our certificates. Let’s Encrypt is a nonprofit, our mission is to create a more secure and privacy-respecting Web by promoting the widespread adoption of HTTPS. Our services are free and easy to use so that every website can deploy HTTPS.

We require support from generous sponsors, grantmakers, and individuals in order to provide our services for free across the globe. If you're interested in supporting us please consider [donating](/donate/) or [becoming a sponsor](/become-a-sponsor/).

In some cases, integrators (e.g. hosting providers) will charge a nominal fee that reflects the administrative and management costs they incur to provide Let’s Encrypt certificates.

## What kind of support do you offer?

Let’s Encrypt is run by a small team and relies on automation to keep costs down. That being the case, we are not able to offer direct support to our subscribers. We do have some great support options though:

1. We have really helpful [documentation](/docs/).
2. We have very active and helpful [community support forums](https://community.letsencrypt.org/). Members of our community do a great job of answering questions, and many of the most common questions have already been answered.

Here's a [video we like](https://www.youtube.com/watch?v=Xe1TZaElTAs) about the power of great community support.

# <a name="technical">Technical Questions</a>

## Are certificates from Let’s Encrypt trusted by my browser?

For most browsers and operating systems, yes. See the [compatibility list](/docs/certificate-compatibility/) for more detail.

## Does Let's Encrypt issue certificates for anything other than SSL/TLS for websites?

Let’s Encrypt certificates are standard Domain Validation certificates, so you can use them for any server that uses a domain name, like web servers, mail servers, FTP servers, and many more.

Email encryption and code signing require a different type of certificate that Let’s Encrypt does not issue.

## Does Let’s Encrypt generate or store the private keys for my certificates on Let’s Encrypt’s servers?

No. Never.

The private key is always generated and managed on your own servers, not by the Let's Encrypt certificate authority.

## What is the lifetime for Let's Encrypt certificates? For how long are they valid?

Our certificates are valid for 90 days. You can read about why [here](https://letsencrypt.org/2015/11/09/why-90-days.html).

There is no way to adjust this, there are no exceptions. We recommend automatically renewing your certificates every 60 days.

## Will Let’s Encrypt issue Organization Validation (OV) or Extended Validation (EV) certificates?

We have no plans to issue OV or EV certificates.

## Can I get a certificate for multiple domain names (SAN certificates or UCC certificates)?

Yes, the same certificate can contain several different names using the Subject Alternative Name (SAN) mechanism.

## Will Let’s Encrypt issue wildcard certificates?

We currently have no plans to do so, but it is a possibility in the future. Hopefully wildcards aren’t necessary for the vast majority of our potential subscribers because it should be easy to get and manage certificates for all subdomains.

## Is there a Let's Encrypt (ACME) client for my operating system?

There are a large number of [ACME clients](/docs/client-options/) available. Chances are something works well on your operating system. We recommend starting with [Certbot](https://certbot.eff.org/).

## Can I use an existing private key or Certificate Signing Request (CSR)?

Yes, but not all clients support this feature. [Certbot](https://certbot.eff.org/) does.

## What IP addresses does Let's Encrypt use to validate my web server?

We don't publish a list of IP addresses we use to validate, because they may change at any time. In the future we may validate from multiple IP addresses at once.
