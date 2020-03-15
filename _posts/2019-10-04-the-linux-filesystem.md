---
layout: post
title: The Linux Filesystem
date: 2019-10-04 19:31:00 -0000
category: chromebook-linux
tags: [linux]
---
# The Linux Filesystem

<ul>
<li>/sbin has your system's essential elements.</li>
<li>/bin has other elements that need to be there though they may not be used.</li>
<li>/usr has most of the applications that you use.</li>
<li>/opt has some self-installed add-on applications.</li>
<li>/etc is where all system configuration files live.</li>
<li>/lib is where all libraries required by your system or applications live.</li>
<li>/media is where the contents of your various attached external media (USB, CD, etc.) appear when connected.</li>
<li>/home
<ul>
<li>This subfolder has all the user accounts for your system.</li>
<li>When you first login you're in your user account's home folder.</li>
<li>If you enter the&nbsp;<b>pwd</b>&nbsp;command (print working directory), you'll see /home/username</li>
</ul>
</ul>
<p>The purpose of the other root folders are less straightforward and shouldn't be tampered with directly.</p>

<h2>Source</h2>
<ul>
<li>Linux book</li>
</ul>
