# Blacklisting a module

add module(s) that will be blacklisted in the blacklist.conf file taht being provided in conf directory.

```
...
blacklist [module-name]
...
```
Use the following format to make sure those module(s) won't be loaded into 
the kernel (using fake install):

```
...
install [module-name] /bin/true
...
```

Please use modinfo command to get a better understanding about the module(s) you wanna know.

Use this command if you've finished the settings.

```
# depmod -ae
# update-initramfs -u
# reboot
```

YOu could use this command, temporarily:

```
chmod +x blacklist-module.sh
./blacklist-module.sh
```

Please read [documentation] 
(https://wiki.debian.org/KernelModuleBlacklisting) for more info  :))
