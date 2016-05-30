---
published: true
title: SSH on Remote Server (Digital Ocean)
layout: post
tags: [ssh]
---
user

    ssh root@SERVER_IP_ADDRESS (logar ssh numa maquina)
    adduser nomeuser
    gpasswd -a nomeuser sudo
    ssh-keygen (local, copy id pub)

at server:

    chmod 700 .ssh
    nano .ssh/authorized_keys
    chmod 600 .ssh/authorized_keys
    exit
    nano /etc/ssh/sshd_config (configure ssh daemon security again root access)

    PermitRootLogin no

    service ssh restart (restarta ssh)