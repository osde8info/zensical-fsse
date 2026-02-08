---
title: "node theia ide quickstart"
date: 2020-02-17
categories: 
  - "fsse"
tags: 
  - "ide"
  - "node"
  - "theia"
---

theia quickstart instructions (including installing nvm node etc etc)

- `wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash`
- (logout and login again ! or source the bash script if you are a pro)
- `nvm install 10`
- `nvm use 10`
- `npm -g install yarn` # (TOPTIP -g means READ and SET options globally)
- `mkdir mytheia`
- `cd mytheia`
- `vi package.json` # (C&P from [https://theia-ide.org/docs/composing\_applications](https://theia-ide.org/docs/composing_applications))
- `yarn` # will autoinstall everything from your package.json
- `yarn theia build` (takes approx 400 seconds)
- `yarn theia start`
- open [http://localhost:3000](http://localhost:3000)

theia full instructions

- [https://github.com/nvm-sh/nvm/blob/master/README.md#install--update-script](https://github.com/nvm-sh/nvm/blob/master/README.md#install--update-script)
- [https://theia-ide.org/docs/composing\_applications/](https://theia-ide.org/docs/composing_applications/)
