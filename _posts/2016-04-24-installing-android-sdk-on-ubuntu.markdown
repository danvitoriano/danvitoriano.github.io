---
published: true
title: Installing Android SDK on Ubuntu
layout: post
tags: [android-sdk, ubuntu]
categories: [android, ]
---
    $ wget http://dl.google.com/android/android-sdk_r20-linux.tgz && tar -xvf android-sdk_r20-linux.tgz
    $ export PATH=${PATH}:~/android-sdk-linux/tools:~/android-sdk-linux/platform-tools
    $ echo -e '\nexport PATH=${PATH}:~/android-sdk-linux/tools:~/android-sdk-linux/platform-tools' >> ~/.bashrc
    $ android