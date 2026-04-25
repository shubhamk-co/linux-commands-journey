\# Linux Basic Definitions



\## 1. Linux

Linux is an open-source operating system based on Unix.

It is used in servers, cybersecurity, cloud, and development.



\---

In Linux there is two type of user.

1. super user(root)

2\. normal user(username) 



\----

In Linux there are two types of data.

1. default data

2\. custom data



\---

In Linux there is no concept of (C:), drive in Linux there is only one directory (/)

(/)==>this directory show only top level data 



/  ====> OS controlling data

&#x20;  ====> User define data





example :-



\[root@localhost \~]# ls /

afs  bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var



\---



If we want to see top user define data .

\->/home/username/

this is where user can define data , out home user can't create any file or folder ,user only can see data as per permission (provider by root ).  



example :-



\[shubham@localhost \~]$ pwd

/home/shubham

\[shubham@localhost \~]$ ls





\## 2. Kernel

Kernel is the core part of the operating system.

It manages hardware and software communication.



\---



\## 3. Shell

Shell is a command-line interface (CLI) used to interact with the system.

Example: Bash



\---



\## 4. Terminal

Terminal is an application used to access the shell and run commands.



\---



\## 5. Command

A command is an instruction given to the system to perform a task.

Example: ls, pwd



\---



\## 6. Directory

A directory is a folder or file used to store files and other directories.



\---



\## 7. Root Directory (/)

The top-most directory in Linux is called root (/).

In Linux there is no disk format just like windows

Example: temp ,bin ,home

or



on windows (C:)

In windows disk format in (C: , D: , E: ,F:)

(C:) ->c drive is a mandatory , in C: drive operating system will store



\---



\## 8. User

A user is a person or account that uses the system.



Types:

\- Root user (admin)

\- Normal user



\---



\## 9. Permission

Permissions control who can read, write, or execute a file.



\---



\## 10. Process

A process is a running program in the system.



\---

