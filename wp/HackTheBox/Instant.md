# Instant

> 本机 IP: 10.10.16.26
>
> 目标 IP: 10.10.11.37

```sh
$ nmap -A 10.10.11.37
Nmap scan report for bogon (10.10.11.37)
Host is up (0.75s latency).
Not shown: 998 closed tcp ports (conn-refused)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 9.6p1 Ubuntu 3ubuntu13.5 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey:
80/tcp open  http    Apache httpd 2.4.58
|_http-title: Did not follow redirect to http://instant.htb/
|_http-server-header: Apache/2.4.58 (Ubuntu)
Service Info: Host: instant.htb; OS: Linux; CPE: cpe:/o:linux:linux_kernel

$ vi /etc/hosts
[+] 10.10.11.33 instant.htb
```
