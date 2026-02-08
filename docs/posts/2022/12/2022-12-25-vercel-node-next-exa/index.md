---
title: "vercel node next examples &amp; demos"
date: 2022-12-25
categories: 
  - "fsse"
---

vercel node next

examples

https://github.com/vercel/next.js/tree/canary/examples  
https://github.com/vercel/next.js/tree/canary/examples/hello-world  
https://github.com/vercel/next.js/tree/canary/examples/blog-starter  
https://github.com/vercel/next.js/tree/canary/examples/github-pages  
https://github.com/vercel/next.js/tree/canary/examples/cms-wordpress  
https://github.com/vercel/next.js/tree/canary/examples/with-jest

demos

  
https://next-blog-starter.vercel.app/  
https://next-blog-wordpress.vercel.app/

try it yourself

stage 1

option 1 dev & run remotely by clicking the https://stackblitz.com/ remotedev link

option 2 dev & run locally

option 3 dev & run in a wsl container

stage 2

push to vercel

## option 1 dev & run remotely

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-22.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-22.png)

# option 2 dev & run locally

## install node

then in a powershell check node & npm are installed and are in the path

installed

```
node -version
v18.12.1

npm -version
8.19.2
```

in path

```
$env:path -Split ";"

C:\WINDOWS\system32
C:\WINDOWS
C:\WINDOWS\System32\Wbem
C:\WINDOWS\System32\WindowsPowerShell\v1.0\
C:\WINDOWS\System32\OpenSSH\
C:\Program Files\Git\cmd
C:\Program Files\nodejs\
C:\Users\clida\AppData\Local\Microsoft\WindowsApps
C:\Users\clida\AppData\Local\Programs\Microsoft VS Code\bin
C:\Users\clida\AppData\Roaming\npm
```

## install pnpm & vercel

```
npm -g install pnpm
npm -g install vercel

npm -g list
C:\Users\clida\AppData\Roaming\npm
+-- pnpm@7.19.0
`-- vercel@28.10.1
```

# enable powershell

```
Get-ExecutionPolicy -List

        Scope ExecutionPolicy
        ----- ---------------
MachinePolicy       Undefined
   UserPolicy       Undefined
      Process       Undefined
  CurrentUser       Undefined
 LocalMachine       Undefined
```

if CurrentUser and LocalMachine are both Undefined then define one of them in an admin powershell

```
Set-ExecutionPolicy RemoteSigned
Get-ExecutionPolicy -List

        Scope ExecutionPolicy
        ----- ---------------
MachinePolicy       Undefined
   UserPolicy       Undefined
      Process       Undefined
  CurrentUser       Undefined
 LocalMachine    RemoteSigned
```

## create and dev

```
pnpm create next-app --example hello-world verc-next-hello-world

cd verc-next-hello-world

pnpm run dev
```

then browse to http://localhost:3000/

## build and start

```
pnpm build
pnpm start
```

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-20.png?w=1024)](https://fsse8info.wordpress.com/wp-content/uploads/2022/12/image-20.png)

![](https://fsse8info.wordpress.com/4a44749b-9c87-485e-8433-01d4a327d32d)
