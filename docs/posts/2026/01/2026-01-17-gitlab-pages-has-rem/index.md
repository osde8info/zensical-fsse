---
title: "GitLab Pages has removed the namespace level Pages settings"
date: 2026-01-17
categories: 
  - "fsse"
---

GitLab Pages has removed the namespace level Pages settings for:

personal accounts

free-tier namespaces

If you deploy Pages from a personal namespace, GitLab assigns a domain like:

[https://XXX.gitlab.io/YYY](https://-.gitlab.io)

This is the new default behaviour.

You only get the clean URL IF YOU PAY

but you can add a domain to a project

The steps are:

Go to your project

Open Settings → Pages (this does exist at the project level)

Add a new domain

GitLab gives you a DNS record

Add it to your DNS provider

GitLab issues a free HTTPS certificate

BUT FIRST

Move your project into a **group namespace** (free).

Groups _do_ still have Pages → Domains.

Add a custom domain

The UI is hidden unless the project is in a **group**.

So again, you must move the project into a group first.

## STOP PRESS

This hashed domain is the **only** domain GitLab will give you on the free plan.

[https://mkdocs-3-d7d8a1.gitlab.io](https://mkdocs-3-d7d8a1.gitlab.io)

You need to switch to GITHUB NETLIFY or VERCEL today for FREE clean URLs !
