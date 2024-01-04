# RHEL Study Guide - Control Access To Files

[RHEL Study Guide - Table of Contents](https://github.com/pslucas0212/RHEL-Study-Guide)  

Make a practice directory
```
# mkdir -p /home/techdocs
```

Change group to techdocs
```
# chown :techdocs /home/techdocs
```

Check if user tech1 can access /home/techdocs, if not modify /home/techdocs to give techdocs group rwx capabilites.  Set sigid to 2 in this ecample.
```
# ls -ls /home/techdocs
# chmod 2770 /home/techdocs
```

Check if users tech1 or tech2 have access, but not database1

Change umask setting for login owner and group have rwx, but other has none.  Go to the /etc/login.defs and modify UMASK
```
UMASK 007
```
