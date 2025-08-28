# The hosts file

Ansible uses its own hosts file to define which machines it will operate on; it is an inventory of all the target servers. Although servers can be defined undifferentiated, it is normal to group them under functional headings. I could define groups as shown below.

I can deal with Ubuntu and CentOS tasks separately, and then also deal with all Apache servers regardless of their base OS.

As you can imagine, the configuration of a real Apache server can be really complicated. Consider that all Web servers these days support HTTPS. When you are standing up a Web Server the chances are, you’re also going to have to copy across keys and certificates and configure them!

```
[UB1804]
UB1.example.com
UB2.example.com 

[CO7]
CO7-1.example.com
CO7-2.example.com 

[Apache]
UB1.example.com
CO7-2.example.com 
```

You can also define groups of groups. In the example above, to address all my learning servers

```
[AllLinux]
CO7
UB1804
```
