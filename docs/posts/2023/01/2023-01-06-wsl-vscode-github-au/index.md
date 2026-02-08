---
title: "wsl vscode github auth is broken ! #webdev"
date: 2023-01-06
categories: 
  - "fsse"
---

actually "vscode 2 wsl github auth" is fine but "vscode in wsl github auth" is broken for both oracle linux 8 & ubuntu linux 18 wsl instances !

theory : might be due to broken gnome keychains

and since aug 2021 you can no longer auth with github user & pass even if you have set your git config values

```
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

so you need to create a token (PAT) or use GCM instead

```
$ git push

Username for 'https://github.com': osde8info
Password for 'https://osde8info@github.com':

remote: Support for password authentication was removed on August 13, 2021.

remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.

fatal: Authentication failed for 'https://github.com/osde8info/astro-vercel-astro.git/'
```

your git push should then work

```
$ git push
Username for 'https://github.com': osde8info
Password for 'https://osde8info@github.com':

Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.

Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 286 bytes | 286.00 KiB/s, done.

Total 3 (delta 2), reused 0 (delta 0), pack-reused 0

remote: Resolving deltas: 100% (2/2), completed with 2 local objects.

To https://github.com/osde8info/astro-vercel-astro.git
   88cabd0..c00be94  main -> main
```

refs

- https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls

- https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

- https://github.com/GitCredentialManager/git-credential-manager/blob/main/README.md
