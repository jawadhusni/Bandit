Terminal
===
```
bandit12@melinda:~$ ls
data.txt
bandit12@melinda:~$ cp data.txt /tmp/temp/.
bandit12@melinda:~$ cd /tmp/temp/
bandit12@melinda:/tmp/temp$ ls
data.txt

bandit12@melinda:/tmp/temp$ xxd -r data.txt > tmp1.gz && gzip -d tmp1.gz && bzip2 -dc tmp1 > tmp2.gz && gzip -d tmp2.gz && tar -xvf tmp2 && tar -xvf data5.bin && bzip2 -d data6.bin && mv data6.bin.out tmp3 && tar -xvf tmp3 && mv data8.bin tmp4.gz && gzip -d tmp4.gz && cat tmp4
gzip: tmp1 already exists; do you wish to overwrite (y or n)? y
gzip: tmp2 already exists; do you wish to overwrite (y or n)? y
data5.bin
data6.bin
bzip2: Can't guess original name for data6.bin -- using data6.bin.out
data8.bin
gzip: tmp4 already exists; do you wish to overwrite (y or n)? y
The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
```
