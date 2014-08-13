Terminal
===
```
andit16@melinda:~$ nmap -Pn localhost -p31000-32000

Starting Nmap 5.21 ( http://nmap.org ) at 2014-08-13 04:42 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.0012s latency).
Not shown: 995 closed ports
PORT      STATE SERVICE
31000/tcp open  unknown
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown


bandit16@melinda:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
depth=0 CN = localhost
verify error:num=18:self signed certificate
verify return:1
depth=0 CN = localhost
verify return:1
---
Certificate chain
 0 s:/CN=localhost
   i:/CN=localhost
---
Server certificate
-----BEGIN CERTIFICATE-----
MIICpDCCAYwCCQDDVcPYicjxQjANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDEwls
b2NhbGhvc3QwHhcNMTMwNjA2MTM1ODM3WhcNMjMwNjA0MTM1ODM3WjAUMRIwEAYD
VQQDEwlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDF
Id/8XRfPayS8u+XfqkXQq3QawTEmxcxQw4TiLKlnqLqsl02U3dUIBqSJu1LQE8lf
/eez2KF9Nse9cXqty6M6J9/515b+xaLfkAV1q97JwO1BfciJDiWqjPerMcikUb0d
zTnDFSpWpnrTjLqlquSWrgRxMffmGi+6x7lsWp8EOAIrFhxadYgTskVUslsgtwBP
dVtDG3OZSa8uyD6LJMCgMpaIs0nI1AS8yWWRnBPP6tujJV9x5JI8GYuC1OB9hsYT
+J7ZMkQ5soOXi9TIuyQSfavH27z44uMF3g4fB6i9l2KNFeKkuq1JVM+HbrXfSlf3
+Gtm/+hO/jlKzGw+pmobAgMBAAEwDQYJKoZIhvcNAQEFBQADggEBAF0ah9QUPxRM
cCNaZ2Bb+IkBXbj1esk92Hv7H4uYIionJl2f+8M6/YgGNhBI4C1r82Hwbi9DwVYs
kztth6DQIBw3KnNLyoKfYmEz6+Azko5rIefeJoHEBdD41tMqmBd8jWi5+hUbkeLr
8A0wzwi/mVQP4xBZ5cELDEaC2MFCi20X4APFFYeXEMjEYwTwADdADiQ52ezle0zr
iSZ10PUmxqjE4NCYo8feZ7emRcAozZElyF9JjoHfXSSiEViELPU2Wb9ygljYz2Hy
AGDcpE2FIGZRiHk+PT2tHD92bp4BeyZsh52pYvItJie3owdIQoQASfperclRvcyn
mNrjHPUubAc=
-----END CERTIFICATE-----
subject=/CN=localhost
issuer=/CN=localhost
---
No client certificate CA names sent
---
SSL handshake has read 1272 bytes and written 375 bytes
---
New, TLSv1/SSLv3, Cipher is DHE-RSA-AES256-SHA
Server public key is 2048 bit
Secure Renegotiation IS supported
Compression: NONE
Expansion: NONE
SSL-Session:
    Protocol  : SSLv3
    Cipher    : DHE-RSA-AES256-SHA
    Session-ID: A73B5DEFA8C51F2DB426EF8146511704FBC1664CEC6E9F5516136C8D96A55ECF
    Session-ID-ctx:
    Master-Key: 08EE2A81B741A1D12C5E6386CF64DD58934BD243CF82541477A973D4BE7E52B5A121C72F1C05A892864EAD142BCB6BAC
    Key-Arg   : None
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    Start Time: 1407905149
    Timeout   : 300 (sec)
    Verify return code: 18 (self signed certificate)
---
cluFn7wTiGryunymYOu4RcffSxQluehd
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

read:errno=0
```
