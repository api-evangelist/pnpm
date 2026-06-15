---
title: "Why pnpm no longer expands environment variables in a repository's .npmrc"
url: "https://pnpm.io/blog/2026/06/11/env-variables-in-repository-npmrc"
date: "2026-06-11"
author: "Zoltan Kochan"
feed_url: "https://pnpm.io/blog/atom.xml"
---
pnpm used to expand $ placeholders everywhere it found them — including in the .npmrc and pnpm-workspace.yaml files that live inside the repository you just cloned. That turned out to be a way for a malicious repository to steal the secrets in your environment. As of v10.34.2 and v11.5.3, pnpm stops expanding environment variables in repository-controlled registry and credential settings.
