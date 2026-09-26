---
aliases:
tags:
  - arch
  - manjaro
  - linux
  - Remote
  - ssh
done: false
created: 2026-05-04
sourse:
---
# Enable SSH Service in Manjaro Linux


**SSH** Service can be enabled and launched on Manjaro in few simple steps using **systemd** commands (release: 16.06 – as of writing this post)

...
Steps:

**1. Install OpenSSH (if needed)**

```bash
[tuxfixer@manjaro ~]$ sudo pacman -S openssh 
```

**Note:** On fresh Manjaro installation OpenSSH service should be installed by default (OS release: 16.06 – as of writing this post).
...
**2. Verify SSH Service status**

```bash
[tuxfixer@manjaro ~]$ sudo systemctl status sshd.service
```

**Note:** OpenSSH service should be disabled by default.
...
**3. Edit SSH Daemon config file (if needed)**

```bash
[tuxfixer@manjaro ~]$ sudo nano /etc/ssh/sshd_config
```
...
**4. Enable and launch SSH Service**

```bash
[tuxfixer@manjaro ~]$ sudo systemctl enable sshd.service
```

```bash
[tuxfixer@manjaro ~]$ sudo systemctl start sshd.service
```
...
**5. Test SSH connectivity**

Try to connect to your Manjaro **SSH** Server from **Client** machine:

```bash
[tuxfixer@client ~]$ ssh tuxfixer@192.168.2.59
The authenticity of host '192.168.2.59 (192.168.2.59)' can't be established.
ECDSA key fingerprint is SHA256:W5Gem3BN7Dyhxm0qUMIQBV6ZI9HnJSYEVEKJtZ7clyg.
ECDSA key fingerprint is MD5:24:ef:a5:07:af:29:0a:e2:20:14:f5:a5:f4:c2:05:38.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '192.168.2.59' (ECDSA) to the list of known hosts.
tuxfixer@192.168.2.59's password: 
[tuxfixer@manjaro ~]$ 
```