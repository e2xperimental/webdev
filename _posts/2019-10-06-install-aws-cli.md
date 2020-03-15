---
layout: post
title: How to install AWS CLI on a Chromebook Acer R 13
date: 2019-10-06 13:00:00 -0000
category: chromebook-linux
tags: [aws, how-to-install]
---
# How to install AWS CLI on a Chromebook Acer R 13

## October 06, 2019

I recommend using the [Bundled package](https://docs.amazonaws.cn/en_us/cli/latest/userguide/install-bundle.html#install-bundle-other) to install the AWS Command Line Interface (AWS CLI) on a Chromebook.

Run these three commands to download and extract the file.

```
curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip"
unzip awscli-bundle.zip
sudo ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws
```

If you get an error when running the third command

`/usr/bin/env: ‘python’: No such file or directory`

Try including the absolute Python path.
Run this command to find out the absolute path of your Python installation.

```
sudo ls -alg /usr/bin/python3.5
-rwxr-xr-x 2 root 4297032 Sep 27  2018 /usr/bin/python3.5
```

Then add your absolute path after "sudo."

```
sudo /usr/bin/python3.5 ./awscli-bundle/install -i /usr/local
/aws -b /usr/local/bin/aws
```

To check that the bundled package was installed successfully, run:

```
/usr/local/bin/aws --version
aws-cli/1.16.253 Python/3.5.3 Linux/4.19.60-06185-g54aa50936831 botocore/1.12.243
```

Sources
- [Installing the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html)
- [Configuring the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html)
