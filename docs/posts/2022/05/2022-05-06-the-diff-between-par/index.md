---
title: "the diff between parallel-ssh -i and parallel-ssh -P"
date: 2022-05-06
categories: 
  - "fsse"
---

the difference between parallel-ssh -i and parallel-ssh -P

```
$ parallel-ssh -H "jenkins1 jenkins2" "echo 'hello';sleep 2;echo 'world'"
[1] 16:02:42 [SUCCESS] jenkins1
[2] 16:02:42 [SUCCESS] jenkins2
```

parallel-ssh -i

```
$ parallel-ssh -i -H "jenkins1 jenkins2" "echo 'hello';sleep 2;echo 'world'" 
[1] 16:02:24 [SUCCESS] jenkins1
hello
world
[2] 16:02:24 [SUCCESS] jenkins2
hello
world
```

parallel-ssh -P

```
$ parallel-ssh -P -H "jenkins1 jenkins2" "echo 'hello';sleep 2;echo 'world'"
jenkins1: hello
jenkins2: hello
jenkins1: world
[1] 16:02:50 [SUCCESS] jenkins1
jenkins2: world
[2] 16:02:51 [SUCCESS] jenkins2
```

advanced usage

```
# echo "set -e -x;echo 'hello';sleep 2;echo 'world'" | parallel-ssh -i -v -H "jenkins1 jenkins2" -I /bin/bash
[1] 16:24:07 [SUCCESS] jenkins2
hello
world
Stderr: + echo hello
+ sleep 2
+ echo world
[2] 16:24:07 [SUCCESS] jenkins1
hello
world
Stderr: + echo hello
+ sleep 2
+ echo world
```
