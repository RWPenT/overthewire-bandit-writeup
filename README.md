# Bandit Write-up

> 🏴‍☠️ **Topic:** Basics of the Linux terminal

**Connection**

```bash
ssh bandit[bandit level]@bandit.labs.overthewire.org -p 2220
```

---

# Level 0 → Level 1

**Level Goal:**

The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

**Commands you may need to solve this level:**

[`ls`](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html), [`cd`](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html), [`cat`](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html), [`file`](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html), [`du`](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html), [`find`](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

I entered the password for Level 0 (`bandit0`) and got access to `bandit0@bandit.labs.overthewire.org` on port 2220.

I entered the following commands and found the password for Level 1.

```bash
ls -la
```

We use the `ls` command to view the contents of a directory, and `-la` shows them in detail (long format, including hidden files).

```
total 24
drwxr-xr-x   2 root    root    4096 Oct 25 13:37 .
drwxr-xr-x 150 root    root    4096 Oct 25 13:40 ..
-rw-r--r--   1 root    root     220 Feb 13  2026 .bash_logout
-rw-r--r--   1 root    root    3851 Oct 25 13:21 .bashrc
-rw-r--r--   1 root    root     807 Feb 13  2026 .profile
-rw-r-----   1 bandit1 bandit0  438 Oct 25 13:37 readme
```

```bash
cat readme
```

`cat` prints the contents of a file.

```
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

The password you are looking for is: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR

```

> 🔑 **Password (Level 1):** `6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR`

---

# Level 1 → Level 2

**Level Goal:**

The password for the next level is stored in a file called `-` located in the home directory

**Commands you may need to solve this level:**

[`ls`](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html), [`cd`](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html), [`cat`](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html), [`file`](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html), [`du`](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html), [`find`](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

```bash
ls -la
```

```
total 24
-rw-r-----   1 bandit2 bandit1   33 Oct 25 13:37 -
drwxr-xr-x   2 root    root    4096 Oct 25 13:37 .
drwxr-xr-x 150 root    root    4096 Oct 25 13:40 ..
-rw-r--r--   1 root    root     220 Feb 13  2026 .bash_logout
-rw-r--r--   1 root    root    3851 Oct 25 13:21 .bashrc
-rw-r--r--   1 root    root     807 Feb 13  2026 .profile
```

```bash
cat ./-
```

```
PK8fYLZg2hnHSz83plBL1iEPKdD3QToB
```

> 🔑 **Password (Level 2):** `PK8fYLZg2hnHSz83plBL1iEPKdD3QToB`

---

# Level 2 → Level 3

**Level Goal:**

The password for the next level is stored in a file called `--spaces in this filename--` located in the home directory

**Commands you may need to solve this level:**

[`ls`](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html), [`cd`](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html), [`cat`](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html), [`file`](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html), [`du`](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html), [`find`](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

```bash
ls -la
```

```
total 24
-rw-r-----   1 bandit3 bandit2   33 Oct 25 13:37 --spaces in this filename--
drwxr-xr-x   2 root    root    4096 Oct 25 13:37 .
drwxr-xr-x 150 root    root    4096 Oct 25 13:40 ..
-rw-r--r--   1 root    root     220 Feb 13  2026 .bash_logout
-rw-r--r--   1 root    root    3851 Oct 25 13:21 .bashrc
-rw-r--r--   1 root    root     807 Feb 13  2026 .profile
```

```bash
cat ./--spaces\ in\ this\ filename--
```

While typing this command, I wrote `cat ./--` and just pressed the Tab key to autocomplete the filename.

```
7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME
```

> 🔑 **Password (Level 3):** `7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME`

---

# Level 3 → Level 4

**Level Goal:**

The password for the next level is stored in a hidden file in the **inhere** directory.

**Commands you may need to solve this level:**

[`ls`](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html), [`cd`](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html), [`cat`](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html), [`file`](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html), [`du`](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html), [`find`](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

```bash
ls -la
```

```
total 24
drwxr-xr-x   3 root root 4096 Oct 25 13:37 .
drwxr-xr-x 150 root root 4096 Oct 25 13:40 ..
-rw-r--r--   1 root root  220 Feb 13  2026 .bash_logout
-rw-r--r--   1 root root 3851 Oct 25 13:21 .bashrc
-rw-r--r--   1 root root  807 Feb 13  2026 .profile
drwxr-xr-x   2 root root 4096 Oct 25 13:37 inhere
```

```bash
cd inhere
```

`cd` is used to change into a directory.

```bash
ls -la
```

```
total 12
drwxr-xr-x 2 root    root    4096 Oct 25 13:37 .
drwxr-xr-x 3 root    root    4096 Oct 25 13:37 ..
-rw-r----- 1 bandit4 bandit3   33 Oct 25 13:37 ...Hiding-From-You
```

```bash
cat ./...Hiding-From-You
```

```
xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq
```

> 🔑 **Password (Level 4):** `xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq`

---

# Level 4 → Level 5

**Level Goal:** The password for the next level is stored in the only human-readable file in the **inhere** directory.

> 💡 Tip: if your terminal is messed up, try the “reset” command.

**Commands you may need to solve this level:**

[`ls`](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html), [`cd`](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html), [`cat`](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html), [`file`](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html), [`du`](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html), [`find`](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

```bash
ls -la
```

```
total 24
drwxr-xr-x   3 root root 4096 Oct 25 13:37 .
drwxr-xr-x 150 root root 4096 Oct 25 13:40 ..
-rw-r--r--   1 root root  220 Feb 13  2026 .bash_logout
-rw-r--r--   1 root root 3851 Oct 25 13:21 .bashrc
-rw-r--r--   1 root root  807 Feb 13  2026 .profile
drwxr-xr-x   2 root root 4096 Oct 25 13:37 inhere
```

```bash
cd inhere
```

```bash
ls -la
```

```
total 48
-rw-r----- 1 bandit5 bandit4   33 Oct 25 13:37 -file00
-rw-r----- 1 bandit5 bandit4   33 Oct 25 13:37 -file01
-rw-r----- 1 bandit5 bandit4   33 Oct 25 13:37 -file02
-rw-r----- 1 bandit5 bandit4   33 Oct 25 13:37 -file03
-rw-r----- 1 bandit5 bandit4   33 Oct 25 13:37 -file04
-rw-r----- 1 bandit5 bandit4   33 Oct 25 13:37 -file05
-rw-r----- 1 bandit5 bandit4   33 Oct 25 13:37 -file06
-rw-r----- 1 bandit5 bandit4   33 Oct 25 13:37 -file07
-rw-r----- 1 bandit5 bandit4   33 Oct 25 13:37 -file08
-rw-r----- 1 bandit5 bandit4   33 Oct 25 13:37 -file09
drwxr-xr-x 2 root    root    4096 Oct 25 13:37 .
drwxr-xr-x 3 root    root    4096 Oct 25 13:37 ..
```

Then I opened them one by one until I found the right one:

```bash
cat ./-file07
```

```
6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
```

> 🔑 **Password (Level 5):** `6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG`

---

# Level 5 → Level 6

**Level Goal:** The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable

**Commands you may need to solve this level:**

[`ls`](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html), [`cd`](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html), [`cat`](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html), [`file`](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html), [`du`](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html), [`find`](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

`find` is a command that searches for files or directories by given criteria. It supports options such as `-type`, `-name` (case-sensitive), `-iname` (case-insensitive), `-size`, `-exec`, `-mtime`, and so on.

For this level, I will use `-size 1033c` (`c` stands for bytes) and `-type f` to find the correct file.

```bash
find -type f -size 1033c
```

```
./inhere/maybehere07/.file2
```

```bash
cat ./inhere/maybehere07/.file2
```

```
pXa26xhMWaC2SvDotA4r9EgZkulOeSBW
```

> 🔑 **Password (Level 6):** `pXa26xhMWaC2SvDotA4r9EgZkulOeSBW`

---

# Level 6 → Level 7

**Level Goal:** The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user `bandit7`
- owned by group `bandit6`
- 33 bytes in size

**Commands you may need to solve this level:**

[`ls`](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html), [`cd`](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html), [`cat`](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html), [`file`](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html), [`du`](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html), [`find`](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html), [`grep`](https://manpages.ubuntu.com/manpages/noble/man1/grep.1.html)

```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

`/` is the root directory of Linux, and I want to search the whole filesystem for this file. `-user bandit7` finds files owned by the user `bandit7`, and `-group bandit6` finds files owned by the group `bandit6`. `2>/dev/null` discards the “Permission denied” error messages.

```
/var/lib/dpkg/info/bandit7.password
```

```bash
cat /var/lib/dpkg/info/bandit7.password
```

```
Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3
```

> 🔑 **Password (Level 7):** `Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3`

---

# Level 7 → Level 8

**Level Goal:** The password for the next level is stored in the file **data.txt** next to the word **millionth.**

**Commands you may need to solve this level:**

`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

```bash
grep -n millionth data.txt
```

`grep` is a command used to search for text inside a file. The `-n` option makes `grep` print the line number along with each matching line.

```
21389:millionth VR1ljMayciFxbnUokuQmJFw6QC9VKtub
```

> 🔑 **Password (Level 8):** `VR1ljMayciFxbnUokuQmJFw6QC9VKtub`

---

# Level 8 → Level 9

**Level Goal:** The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

**Commands you may need to solve this level:**

`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

```bash
sort data.txt | uniq -u
```

`uniq` filters out repeated lines (don’t forget: `uniq` only detects adjacent duplicates, so the input must be sorted with `sort` first). `-u` prints only the lines that occur exactly once.

```
EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl
```

> 🔑 **Password (Level 9):** `EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl`

---

# Level 9 → Level 10

**Level Goal:** The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

**Commands you may need to solve this level:**

`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

First, I want to see what’s in it.

```bash
cat data.txt
```

I found out that this file contains unreadable binary data, like this:

```
v����n�Z.|H�.�� l��ŕxg���o<�,�ȫ)
```

Because of that, I used the `strings` command, which extracts human-readable strings from non-text files.

```bash
strings data.txt
```

```
Z.|H
*IsU
_WnZ
tv3$Y
y`Y@
fk:@
aAb{
#|bsG
OWCb
'}.0
4LSwe
vLqjp
c]8{
[@fhq-
C(z?U
HKp:D
`=Sc
}7;========== the
$3/y
>RYV
r:+YS
l|-n
G,rD%_
@ttb:
o!2D
`f*
s0q6;
<rOz
cG}RK&
b_cZ
)oO#5
-c=,
\(\(
=9lj
1R7h
pI9d
Xzmb!
CexJ]
6-JycW
GMH@!
NgEU
BIQ7
%4KyMB
O+po
|KK2.
G)IT
fS5`
sf9y    A
$ViS
`f:r]
W;GrGH
y5      C4
daZ-
k0?Z
J,C{
u7FD'
E~*6
fT1<
@ j,~
%1o-
X(Mt
&+E
1d^]6-
========== password
(4K3
ZKbg}z$
0;nQ!
-%N8
9K]|
7O&,
83lW
$ ]w
h@k.
^vx
;n#*
<aVu
IZJ9^
$B33iH
(!#.
/7c~F
%HjS
R8m}w
Oj(%qy=
)PcYa
        /rG%
========== is
'vHS8,
N,qOK
Wn4y
J[f]"
x KA
R$2-
(U!x.
        2_~#
<Qg
>dP8
?n:8.Wm
ckL^
YJ"N,
g1aSD
dRfb
'2F@{f
b0'#}
gTvlG.
Nr^\
N.5     ,#
V )8
/\d{
m RI
(0g_3
D]!F
Dm#h
y8R
        5}@A
;2DD
]-;@
dU5]
M       J`
c53'
iFv9P_
^j^j
>.d+
%)q-1
9u!Dw(
dNLgc
S=/D
=av|
V`Y6DCT,@
+@n@
0=6%J3^7
GdYz;*
|ZV     1
p/I|E
t_qS
v#}n
[([Hx!
X|}2
2Hk0
9nDQ
Ne-wN
M)g9
#(^g]m
aI7c72|
G'SZ
%gSES
'/P3:
bD8sp
@X6m
^BPv
ab={
8R&L
.xo}
(,l#
hdqo
`O>X4
yR9Y/
c}.s
B=e"
W:;Jo
|5Z*
f(ac
4nAM
+3d .|
s+^tf
E/4|
xS2&
p}qEMK
teqi|X;^
4T%KZ
4%?5
H)yy
>]8i
ik<T
>Tc'
1{_e41
6?>!gU
L'S<,
CUnb
qdyd
~_Gb
3x3U
TyAB
6xHq
SFJW
Yq!6
<LJq
5nO$$vp![.
S.K3
`{2
|c%z
{xl+N
        'RSd
]?a"
X_7^
:'RO
Fy=W
`.KdIX
========== B0s2khmbT9u0geKuOoVGW3JZKhndE3BG
LjFCj
X|&O
yS@1Q
v}|S
A8Z#f
ctx#H
8{=9
g^U2
O]'/
P\Y~
81xH
fw~z
D:Fiwa
_&LC
"0Pf
,9{$
CnX|
DHxq!\
9"=>-"
J='h
T1h,wxu
f5s<
O+b)
f}L|
,KaI
J!iu
cqd{03KL
m(g)w
L       *8
o;`;|
}j7H
{ 1c
%5kY
u'4`n
Q_g'
J?L<n
h(,AzF
zX#dG:Q
(jG|P@
qo]Leb
Da}K
t/Pjw
|37n
RiS{
CmMA
iNs!@
M1eR
E`-$
```

As you can see, all the readable words are located after several equals (`=`) signs. That’s why I used `grep`.

```bash
strings data.txt | grep "=="
```

```
}7;========== the
========== password
========== is
========== B0s2khmbT9u0geKuOoVGW3JZKhndE3BG
```

> 🔑 **Password (Level 10):** `B0s2khmbT9u0geKuOoVGW3JZKhndE3BG`

---

# Level 10 → Level 11

**Level Goal:** The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

**Commands you may need to solve this level:**

`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

`base64` is a command for encoding and decoding data. I will use it with the `-d` option to decode.

```bash
cat data.txt | base64 -d
```

```
The password is pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro
```

> 🔑 **Password (Level 11):** `pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro`

---

# Level 11 → Level 12

**Level Goal:** The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

**Commands you may need to solve this level:**

`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

**1. What is ROT13?**

ROT13 (“Rotate by 13 places”) is a simple substitution cipher. Because the English alphabet has 26 letters:

$$
\text{Shift} = 13 \implies 13 + 13 = 26 \equiv 0 \pmod{26}
$$

- ROT13 is **symmetric**: Encrypting and decrypting use the exact same key mapping.
- Shifting forward by 13 positions produces the exact same result as shifting backward by 13 positions.

**2. How `tr` works**

The `tr SET1 SET2` command maps each input character found in `SET1` to the character at the corresponding position in `SET2`.

| Section | SET 1 (Input) | SET 2 (Output) | Logic |
| --- | --- | --- | --- |
| **Lowercase 1st Half** | `a-m` | `n-z` | Shifts forward by 13 |
| **Lowercase 2nd Half** | `n-z` | `a-m` | Wraps around to start |
| **Uppercase 1st Half** | `A-M` | `N-Z` | Shifts forward by 13 |
| **Uppercase 2nd Half** | `N-Z` | `A-M` | Wraps around to start |

```bash
cat data.txt | tr 'a-zA-Z' 'n-za-mN-ZA-M'
```

```
The password is GROozWPO8QyN0mGrjUkID0WCYkZiQxrN
```

> 🔑 **Password (Level 12):** `GROozWPO8QyN0mGrjUkID0WCYkZiQxrN`

---

# Level 12 → Level 13

**Level Goal:** The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

**Commands you may need to solve this level:**

`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`, `mkdir`, `cp`, `mv`, `file`

**Helpful Reading Material:**

[Hex dump on Wikipedia](https://en.wikipedia.org/wiki/Hex_dump)

```bash
cat data.txt
```

```
00000000: 1f8b 0808 0106 de6a 0203 6461 7461 322e  .......j..data2.
00000010: 6269 6e00 0144 02bb fd42 5a68 3931 4159  bin..D...BZh91AY
00000020: 2653 59a8 daa2 ec00 0018 7fff ffeb d7ea  &SY.............
00000030: fffd ffdb bfd2 fbff bdff edfb af1e dfa7  ................
00000040: bffb fd77 3f9c 33eb e1fe ffff b001 3b56  ...w?.3.......;V
00000050: 6881 a680 0000 d034 0000 d034 0680 d320  h......4...4...
00000060: 0d19 069a 0069 a0d0 000d 0343 2000 1903  .....i.....C ...
00000070: 2680 0340 00f2 8da9 8daa 1c9a 0c80 6834  &..@..........h4
00000080: 001a 0d18 8d00 6800 1a00 6819 01e8 4062  ......h...h...@b
00000090: 7a80 6832 0340 7a6a 1a34 340d 0310 1a01  z.h2.@zj.44.....
000000a0: a001 a000 194c 8068 d01a 000d 0000 d00d  .....L.h........
000000b0: 190c 9a00 0680 0d00 001e a1a3 d434 d00d  .............4..
000000c0: 0346 8d00 07a8 3d43 401e a1ea 03d4 f500  .F....=C@.......
000000d0: 680b 6480 3848 04a8 177a 2850 14ce 6f4f  h.d.8H...z(P..oO
000000e0: 1a7c 842c 2195 0a7c d3d3 bdc8 6471 d5c2  .|.,!..|....dq..
000000f0: 907f 3d3e 4721 7075 afd2 d84d beac f3bd  ..=>G!pu...M....
00000100: f75e abd3 66d7 859f 7641 e88c e6fa 17de  .^..f...vA......
00000110: 588b 67eb 37f2 4293 4b55 245a 08ce 3840  X.g.7.B.KU$Z..8@
00000120: cfe7 d4a4 0584 2c07 a5fe 7019 25eb 8d6c  ......,...p.%..l
00000130: ce6c 6028 10b8 8994 a318 84c6 2769 0633  .l`(........'i.3
00000140: 1890 98e1 2194 c4cd 48ed 17fc 5781 b243  ....!...H...W..C
00000150: a82b db82 de7f 2045 1ead 30b0 552a abaf  .+.... E..0.U*..
00000160: 673d 9750 c45c a351 a513 9976 ee1c a2d8  g=.P.\.Q...v....
00000170: 6400 a5e4 d4f0 4c54 601e 2700 156f accb  d.....LT`.'..o..
00000180: c2ac 20be a8f8 a98f a8ad c9bb 0c22 68dc  .. .........."h.
00000190: 0083 4d18 49e1 c993 fe6a 49f8 461a e054  ..M.I....jI.F..T
000001a0: 4d05 9cfc 3c8a 0e2f c706 750a 82e3 d30c  M...<../..u.....
000001b0: 20ee 4095 17c2 4efe 432f e10b d5d1 afa4   .@...N.C/......
000001c0: 34e8 69e2 8453 419d ea83 d29d 6158 fcdf  4.i..SA.....aX..
000001d0: 93e9 742d 2d4a 4ba6 a84b cd85 b687 b59f  ..t--JK..K......
000001e0: e949 2314 bdce ad3f a904 169a dce0 a65c  .I#....?.......\
000001f0: dfd1 8e89 f980 618e 87ec 8a58 11e8 0a5d  ......a....X...]
00000200: cd12 260a 9ae6 5808 72c7 8523 27c4 ea8a  ..&...X.r..#'...
00000210: f818 e755 1ee5 4063 684e b440 11ae e8ce  ...U..@chN.@....
00000220: eb61 17c1 db8f b969 b059 4f06 c803 6223  .a.....i.YO...b#
00000230: 6378 a634 30ad e9f0 0f39 4308 2559 c852  cx.40....9C.%Y.R
00000240: c6b8 1500 6d7a a3c2 ab61 ec16 b973 1128  ....mz...a...s.(
00000250: 0dff 8bb9 229c 2848 546d 5176 00b7 c66d  ....".(HTmQv...m
00000260: 4044 0200 00                             @D...
```

First, we’ll create a working directory in `/tmp`.

```bash
mkdir /tmp/example
```

```bash
cp data.txt /tmp/example/
```

```bash
cd /tmp/example
```

As we saw in the Wikipedia material, the file consists of hexadecimal numbers. We need to convert it back to binary with `xxd`; the `-r` option reverses the hexdump. `>` redirects the output into another file.

```bash
xxd -r data.txt > data
```

If we open the data file, we can’t read anything, so first we should determine the file type. The `file` command helps us identify the exact type.

```bash
file data
```

```
data: gzip compressed data, was "data2.bin", last modified: Sun Oct 25 13:37:05 2026, max compression, from Unix, original size modulo 2^32 580
```

It was compressed with `gzip`. `gzip` is a command for compressing files, and it can also decompress them with the `-d` option.

If we try to decompress it now, we will get an error.

```bash
gzip -d data
```

```
gzip: data: unknown suffix -- ignored
```

This happens because `gzip` won’t decompress a file without the `.gz` extension. That’s why we rename the file and add the `.gz` extension.

The `mv` command is used for renaming.

```bash
mv data data.gz
```

```bash
gzip -d data.gz
```

```bash
ls
```

```
data  data.txt
```

```bash
cat data
```

```
C &�@򍩍��SY�ڢ���������ۿ��������ߧ���w?�3������;Vh����4�4��
���L�h�␦�h2@zj␦44
F��=C@����h
           d�8H�z(P�oO␦|�,!�
|�ӽ�dq�=>G!pu���M����^��fׅ�vA����X�g�7�B�KU$�8@��Ԥ�,��p%�l�l`(������'i3���!���H��W��C�+ۂ� E�0�U*��g=�P�\�Q��v���d����LT`'o��¬ �������ɻ
             "h��MI�ɓ�jI�F␦�TM��<�/�u
���
    �@��N�C/�
             �ѯ�4�i�SA��ҝaX�ߓ�t--JK��Kͅ�����I#�έ?����\�ю���a���X�
]�&
���"�(HTmQv
```

It is another compressed binary file. Let’s check it:

```bash
file data
```

```
data: bzip2 compressed data, block size = 900k
```

We can see that this file has been compressed more than once.

`bzip2` is another file compressor. To decompress, we use the `-d` option.

But first we must add the `.bz2` extension with `mv`.

```bash
mv data data.bz2
```

```bash
bzip2 -d data.bz2
```

```bash
ls
```

```
data  data.txt
```

```bash
file data
```

```
data: gzip compressed data, was "data4.bin", last modified: Sun Oct 25 13:37:05 2026, max compression, from Unix, original size modulo 2^32 20480
```

It is another file compressed with `gzip`. Let’s repeat the `gzip` decompression steps.

```bash
 mv data text.gz
```

```bash
gzip -d text.gz
```

```bash
ls
```

```
data.txt  text
```

```bash
file text
```

```
text: POSIX tar archive (GNU)
```

It is an archive created with `tar`. To extract it, we run `tar xf` after adding the `.tar` extension.

```bash
mv text text.tar
```

```bash
tar xf text.tar
```

```bash
ls
```

```
data.txt  data5.bin  text.tar
```

The new file is `data5.bin`. Let’s check its type.

```bash
file data5.bin
```

```
data5.bin: POSIX tar archive (GNU)
```

Again, we repeat the previous steps.

```bash
mv data5.bin data5.tar
```

```bash
tar xf data5.tar
```

```bash
ls
```

```
data.txt  data5.tar  data6.bin  text.tar
```

Let’s check the type of `data6.bin`.

```bash
file data6.bin
```

```
data6.bin: bzip2 compressed data, block size = 900k
```

As you can see, it is another `bzip2` compressed file, so we repeat the `bzip2` decompression steps.

But don’t forget to add the appropriate extension.

```bash
mv data6.bin data6.bz2
```

```bash
bzip2 -d data6.bz2
```

```bash
file data6
```

```
data6: POSIX tar archive (GNU)
```

`data6` is also a tar archive, so we apply the appropriate steps again.

```bash
mv data6 data6.tar
```

```bash
tar xf data6.tar
```

```bash
ls
```

```
data.txt  data5.tar  data6.tar  data8.bin  text.tar
```

`data8.bin` is a new file. Let’s apply `file` to find out its type.

```bash
file data8.bin
```

```
data8.bin: gzip compressed data, was "data9.bin", last modified: Sun Oct 25 13:37:05 2026, max compression, from Unix, original size modulo 2^32 49
```

This file is `gzip` compressed data, so we decompress it again with the proper steps.

```bash
mv data8.bin data8.gz
```

```bash
gzip -d data8.gz
```

```bash
file data8
```

```bash
data8: ASCII text
```

Finally, we have the correct file. Let’s read the password.

```bash
cat data8
```

```
The password is qQYQiHOBPR8zR61qxYqX45quvihF2uzk
```

> 🔑 **Password (Level 13):** `qQYQiHOBPR8zR61qxYqX45quvihF2uzk`

---

# Level 13 → Level 14

**Level Goal:**

The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.
If you need help with this level: a hint file can be found in the home directory.
Make sure to read the error messages as they are informative.

**Commands you may need to solve this level:**

`ssh`, `scp`, `umask`, `chmod`, `cat`, `nc`, `install`

**Helpful Reading Material:**

[SSH/OpenSSH/Keys](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)

[Transferring Files via SCP](https://help.ubuntu.com/community/SSH/TransferFiles)

First, we view the home directory with `ls`.

```bash
ls
```

```
HINT  sshkey.private
```

The second file is the private key of `bandit14`, and it is needed to connect to the next level.

That’s why we will copy this file with `scp`. Before that, I need to create an empty file named `bandit14.key` on my local Linux machine with `touch`.

```bash
touch bandit14.key
```

Then run `scp` from the local terminal:

```bash
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private ./bandit14.key
```

After the transfer, let’s adjust the permissions of `bandit14.key` with `chmod 600`, because SSH refuses to use a private key whose permissions are too open.

```bash
chmod 600 bandit14.key
```

Finally, we can log in via SSH as `bandit14`.

```bash
ssh -i bandit14.key bandit14@bandit.labs.overthewire.org -p 2220
```

To continue, I need the password of `bandit14`. It can be found in the `/etc` directory.

```bash
cd /etc
```

```bash
ls
```

```
ModemManager                   dhcpcd.conf         issue.bandit.localhost      libnl-3                 passwd         subuid-
PackageKit                     dpkg                issue.behemoth              locale.conf             passwd-        sudo.conf
X11                            dput.cf             issue.behemoth.fail         locale.gen              perl           sudo_logsrvd.conf
acpi                           dracut.conf         issue.behemoth.localhost    localtime               pki            sudoers
adduser.conf                   dracut.conf.d       issue.drifter               logcheck                plymouth       sudoers.d
alternatives                   drifter_pass        issue.drifter.fail          login.defs              pm             supercat
apparmor                       e2scrub.conf        issue.drifter.localhost     logrotate.conf          polkit-1       supervisor
apparmor.d                     ec2_version         issue.formulaone            logrotate.d             ppp            sysctl.conf
apport                         emacs               issue.formulaone.fail       lsb-release             profile        sysctl.d
apt                            environment         issue.formulaone.localhost  ltrace.conf             profile.d      sysstat
bandit_pass                    ethertypes          issue.krypton               lvm                     protocols      systemd
bash.bashrc                    fonts               issue.krypton.fail          machine-id              python3        terminfo
bash_completion                formulaone_pass     issue.krypton.localhost     magic                   python3.14     tmpfiles.d
bash_completion.d              fstab               issue.leviathan             magic.mime              rc0.d          tpm2-tss
behemoth_pass                  fuse.conf           issue.leviathan.fail        manpage_pass            rc1.d          ubuntu-advantage
bindresvport.blacklist         fwupd               issue.leviathan.localhost   manpath.config          rc2.d          ucf.conf
binfmt.d                       gai.conf            issue.manpage               maze_pass               rc3.d          udev
ca-certificates                gdb                 issue.manpage.fail          mdadm                   rc4.d          udisks2
ca-certificates.conf           gitconfig           issue.manpage.localhost     mime.types              rc5.d          ufw
ca-certificates.conf.dpkg-old  glvnd               issue.maze                  mke2fs.conf             rc6.d          update-manager
chrony                         gnutls              issue.maze.fail             modprobe.d              rcS.d          update-motd.d
cloud                          gprofng.rc          issue.maze.localhost        modules                 resolv.conf    update-notifier
console-setup                  groff               issue.narnia                modules-load.d          rmt            usb_modeswitch.conf
cowpoke.conf                   group               issue.narnia.fail           motd                    rpc            usb_modeswitch.d
credstore                      group-              issue.narnia.localhost      mtab                    rsyslog.conf   utumno_pass
credstore.encrypted            grub.d              issue.net                   multipath               rsyslog.d      vconsole.conf
cron.d                         gshadow             issue.utumno                multipath.conf          screenrc       vim
cron.daily                     gshadow-            issue.utumno.fail           nanorc                  security       vmware-tools
cron.hourly                    gss                 issue.utumno.localhost      narnia_pass             selinux        vortex_pass
cron.monthly                   gtk-3.0             issue.vortex                needrestart             sensors.d      vtrgb
cron.weekly                    hdparm.conf         issue.vortex.fail           netconfig               sensors3.conf  vulkan
cron.yearly                    hibinit-config.cfg  issue.vortex.localhost      netplan                 services       watchdog.conf
crontab                        host.conf           kernel                      network                 sgml           wgetrc
crypttab                       hostname            krypton_pass                networkd-dispatcher     shadow         xattr.conf
dbus-1                         hosts               landscape                   networks                shadow-        xdg
dconf                          hosts.allow         ld.so.cache                 newt                    shells         xinetd.conf
debconf.conf                   hosts.deny          ld.so.conf                  nftables.conf           skel           xinetd.d
debian_version                 init.d              ld.so.conf.d                nsswitch.conf           sos            xml
debuginfod                     initramfs-tools     ldap                        opt                     ssh            zsh_command_not_found
default                        inputrc             legal                       os-release              ssl
deluser.conf                   iscsi               leviathan_pass              overlayroot.conf        stunnel
depmod.d                       issue               libaudit.conf               overlayroot.local.conf  subgid
devscripts.conf                issue.bandit        libblockdev                 pam.conf                subgid-
dhcp                           issue.bandit.fail   libibverbs.d                pam.d                   subuid
```

There is a folder that may hold all the Bandit passwords.

```bash
cd bandit_pass
```

```bash
ls
```

```
bandit0   bandit11  bandit14  bandit17  bandit2   bandit22  bandit25  bandit28  bandit30  bandit33  bandit6  bandit9
bandit1   bandit12  bandit15  bandit18  bandit20  bandit23  bandit26  bandit29  bandit31  bandit4   bandit7
bandit10  bandit13  bandit16  bandit19  bandit21  bandit24  bandit27  bandit3   bandit32  bandit5   bandit8
```

```bash
cat bandit14
```

```
aaWecNkG4FhxJQxz07uiwzVP6bJiYS65
```

> 🔑 **Password (Level 14):** `aaWecNkG4FhxJQxz07uiwzVP6bJiYS65`

---

# Level 14 → Level 15

**Level Goal:** The password for the next level can be retrieved by submitting the
password of the current level to **port 30000 on localhost**.

**Commands you may need to solve this level:**

`ssh`, `telnet`, `nc`, `openssl`, `s_client`, `nmap`

**Helpful Reading Material:**

[How the Internet works in 5 minutes (YouTube)](https://www.youtube.com/watch?v=7_LPdttKXPc) (Not completely
accurate, but good enough for beginners)

[IP Addresses](https://computer.howstuffworks.com/web-server5.htm)

[IP Address on Wikipedia](https://en.wikipedia.org/wiki/IP_address)

[Localhost on Wikipedia](https://en.wikipedia.org/wiki/Localhost)

[Ports](https://computer.howstuffworks.com/web-server8.htm)

[Port (computer networking) on Wikipedia](https://en.wikipedia.org/wiki/Port_(computer_networking))

To connect to port 30000 on localhost, we use `nc`, which stands for netcat.

```bash
nc localhost 30000
aaWecNkG4FhxJQxz07uiwzVP6bJiYS65
```

```
Correct!
pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7
```

> 🔑 **Password (Level 15):** `pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7`

---

# Level 15 → Level 16

**Level Goal:** The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL/TLS encryption.

**Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.**

**Commands you may need to solve this level:**
`ssh`, `telnet`, `nc`, `openssl`, `s_client`, `nmap`, `netstat`, `ss`

**Helpful Reading Material:**
- [Secure Socket Layer/Transport Layer Security on Wikipedia](https://en.wikipedia.org/wiki/Transport_Layer_Security)
- [OpenSSL Cookbook - Testing with OpenSSL](https://www.feistyduck.com/library/openssl-cookbook/online/testing-with-openssl/index.html)

To connect to port 30001, `nc` does not work because this port requires SSL/TLS encryption. Instead, we use `openssl` with `s_client` to establish an encrypted connection.

Also, if we paste a password directly in interactive mode and it starts with `R` or `K`, `openssl` treats it as a connected command (`RENEGOTIATING` or `KEYUPDATE`). To avoid this and keep the connection open until the server responds, we send the password using `echo` with `-ign_eof`:

```bash
echo "pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7" | openssl s_client -connect localhost:3001 -ign_eof
```

```
Connecting to 127.0.0.1
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN=SnakeOil
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN=SnakeOil
verify return:1
---
Certificate chain
 0 s:CN=SnakeOil
   i:CN=SnakeOil
   a:PKEY: RSA, 4096 (bit); sigalg: sha256WithRSAEncryption
   v:NotBefore: Jun 10 03:59:50 2024 GMT; NotAfter: Jun  8 03:59:50 2034 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIFBzCCAu+gAwIBAgIUBLz7DBxA0IfojaL/WaJzE6Sbz7cwDQYJKoZIhvcNAQEL
BQAwEzERMA8GA1UEAwwIU25ha2VPaWwwHhcNMjQwNjEwMDM1OTUwWhcNMzQwNjA4
MDM1OTUwWjATMREwDwYDVQQDDAhTbmFrZU9pbDCCAiIwDQYJKoZIhvcNAQEBBQAD
ggIPADCCAgoCggIBANI+P5QXm9Bj21FIPsQqbqZRb5XmSZZJYaam7EIJ16Fxedf+
jXAv4d/FVqiEM4BuSNsNMeBMx2Gq0lAfN33h+RMTjRoMb8yBsZsC063MLfXCk4p+
09gtGP7BS6Iy5XdmfY/fPHvA3JDEScdlDDmd6Lsbdwhv93Q8M6POVO9sv4HuS4t/
jEjr+NhE+Bjr/wDbyg7GL71BP1WPZpQnRE4OzoSrt5+bZVLvODWUFwinB0fLaGRk
GmI0r5EUOUd7HpYyoIQbiNlePGfPpHRKnmdXTTEZEoxeWWAaM1VhPGqfrB/Pnca+
vAJX7iBOb3kHinmfVOScsG/YAUR94wSELeY+UlEWJaELVUntrJ5HeRDiTChiVQ++
wnnjNbepaW6shopybUF3XXfhIb4NvwLWpvoKFXVtcVjlOujF0snVvpE+MRT0wacy
tHtjZs7Ao7GYxDz6H8AdBLKJW67uQon37a4MI260ADFMS+2vEAbNSFP+f6ii5mrB
18cY64ZaF6oU8bjGK7BArDx56bRc3WFyuBIGWAFHEuB948BcshXY7baf5jjzPmgz
mq1zdRthQB31MOM2ii6vuTkheAvKfFf+llH4M9SnES4NSF2hj9NnHga9V08wfhYc
x0W6qu+S8HUdVF+V23yTvUNgz4Q+UoGs4sHSDEsIBFqNvInnpUmtNgcR2L5PAgMB
AAGjUzBRMB0GA1UdDgQWBBTPo8kfze4P9EgxNuyk7+xDGFtAYzAfBgNVHSMEGDAW
gBTPo8kfze4P9EgxNuyk7+xDGFtAYzAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3
DQEBCwUAA4ICAQAKHomtmcGqyiLnhziLe97Mq2+Sul5QgYVwfx/KYOXxv2T8ZmcR
Ae9XFhZT4jsAOUDK1OXx9aZgDGJHJLNEVTe9zWv1ONFfNxEBxQgP7hhmDBWdtj6d
taqEW/Jp06X+08BtnYK9NZsvDg2YRcvOHConeMjwvEL7tQK0m+GVyQfLYg6jnrhx
egH+abucTKxabFcWSE+Vk0uJYMqcbXvB4WNKz9vj4V5Hn7/DN4xIjFko+nREw6Oa
/AUFjNnO/FPjap+d68H1LdzMH3PSs+yjGid+6Zx9FCnt9qZydW13Miqg3nDnODXw
+Z682mQFjVlGPCA5ZOQbyMKY4tNazG2n8qy2famQT3+jF8Lb6a4NGbnpeWnLMkIu
jWLWIkA9MlbdNXuajiPNVyYIK9gdoBzbfaKwoOfSsLxEqlf8rio1GGcEV5Hlz5S2
txwI0xdW9MWeGWoiLbZSbRJH4TIBFFtoBG0LoEJi0C+UPwS8CDngJB4TyrZqEld3
rH87W+Et1t/Nepoc/Eoaux9PFp5VPXP+qwQGmhir/hv7OsgBhrkYuhkjxZ8+1uk7
tUWC/XM0mpLoxsq6vVl3AJaJe1ivdA9xLytsuG4iv02Juc593HXYR8yOpow0Eq2T
U5EyeuFg5RXYwAPi7ykw1PW7zAPL4MlonEVz+QXOSx6eyhimp1VZC11SCg==
-----END CERTIFICATE-----
subject=CN=SnakeOil
issuer=CN=SnakeOil
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: rsa_pss_rsae_sha256
Negotiated TLS1.3 group: X25519MLKEM768
---
SSL handshake has read 3191 bytes and written 1613 bytes
Verification error: self-signed certificate
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Protocol: TLSv1.3
Server public key is 4096 bit
This TLS version forbids renegotiation.
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 18 (self-signed certificate)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 5AACB06EBB81461A07F2C2019FB7D112FE90D55AFB62B38D5BA944D26422C887
    Session-ID-ctx: 
    Resumption PSK: C578229F22F036093B5543BD4893D2FE0F17F78491F08B30E0F3976A6FD748C892AC3D95E5592E93B403681AAD8F3479
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 2b 61 06 c3 d2 aa 12 8f-a3 b9 77 12 07 37 b7 6e   +a........w..7.n
    0010 - 9c 2b e9 ca 92 f7 d9 70-68 7f ac b9 3e a6 b9 35   .+.....ph...>..5
    0020 - 6d 32 44 b5 9e f7 e2 d7-b7 93 ae 41 46 34 48 bb   m2D........AF4H.
    0030 - da fc 4e ff d6 87 50 11-6a de 41 63 da 8d 15 44   ..N...P.j.Ac...D
    0040 - bf bb 04 c6 e3 bd 8f 5e-33 c6 65 56 7a b9 4b 4d   .......^3.eVz.KM
    0050 - a6 2f e9 52 e9 21 4c ef-23 7d ef 09 e3 f1 51 87   ./.R.!L.#}....Q.
    0060 - dc b8 85 c1 71 93 67 ee-62 d7 23 40 a1 4a 46 6b   ....q.g.b.#@.JFk
    0070 - 29 84 d5 ca f6 35 fc 35-48 d1 11 c3 c6 cf f3 82   )....5.5H.......
    0080 - 10 dc 1d 84 ff 7c eb a6-c2 b5 4d 92 d6 3b 94 0e   .....|....M..;..
    0090 - 20 9a 18 cf 11 2b c6 49-00 bc b1 19 f3 36 61 aa    ....+.I.....6a.
    00a0 - a9 23 be 01 0f f3 9d 91-dc 0f 07 9c 51 a4 a4 4d   .#..........Q..M
    00b0 - 52 df 56 e9 3d 16 52 ce-40 15 9c e0 46 b2 d5 8c   R.V.=.R.@...F...
    00c0 - ef 2c 14 cf f9 da 77 93-29 4e 04 a3 8b e7 7e 0e   .,....w.)N....~.
    00d0 - 39 46 59 50 fb ea 54 53-0f 1f be 8e 0e 94 5b 67   9FYP..TS......[g

    Start Time: 1794473664
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 204DB107A166919ACE9D939E945425316D4AC16034629D4FF485A712783B954A
    Session-ID-ctx: 
    Resumption PSK: 5FC9762CAFB3D8D95F2A014C8888AB338F5CDF623836758797BE61CDBBA88E2457C328B846D799DC922B40583B67547C
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 2b 61 06 c3 d2 aa 12 8f-a3 b9 77 12 07 37 b7 6e   +a........w..7.n
    0010 - 5f ab a6 8f 28 86 85 e4-5a 98 7a 07 c3 1e a6 5c   _...(...Z.z....\
    0020 - 06 d4 b1 9c db 41 0d 18-90 bc c9 32 6b 9d 38 92   .....A.....2k.8.
    0030 - b6 83 f0 e6 d5 fa 2b 01-82 bb 8d d4 d4 8d 04 d3   ......+.........
    0040 - 78 6d 61 14 3a b2 48 74-0c 4a 82 52 da 0a 92 67   xma.:.Ht.J.R...g
    0050 - 90 4b 48 68 3d b6 e3 cd-2b 03 8f 1a 72 8a 70 98   .KHh=...+...r.p.
    0060 - f8 cc c7 61 1f 67 1e 04-bb 78 6a 39 8d 30 8d b7   ...a.g...xj9.0..
    0070 - 7f f9 75 61 32 f6 1a d2-1c e9 74 9c dd a2 5e be   ..ua2.....t...^.
    0080 - 93 d5 28 29 28 97 53 ef-61 e7 bc 8d f9 c7 dc dc   ..()(.S.a.......
    0090 - aa 8e c8 0f 7e 6b 2a 68-4f 9a 79 34 2c 54 d2 06   ....~k*hO.y4,T..
    00a0 - 22 a9 44 e4 fd 38 cb d2-55 9a 02 bb f2 15 eb 53   ".D..8..U......S
    00b0 - 71 1e 33 62 e7 8a 07 47-be 47 f3 e6 39 bd e6 51   q.3b...G.G..9..Q
    00c0 - 94 ad 34 44 24 9b bc f9-49 ed 9e c4 bf 58 e9 ec   ..4D$...I....X..
    00d0 - 75 d8 a0 08 a9 6d 02 72-f0 09 26 d3 0f bb 6e 6a   u....m.r..&...nj

    Start Time: 1794473664
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
Correct!
kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V

closed
```

> 🔑 **Password (Level 16):** `kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V`

---

# Level 16 → Level 17

**Level Goal:** The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

**Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.**

**Commands you may need to solve this level:**
`ssh`, `telnet`, `nc`, `openssl`, `s_client`, `nmap`, `netstat`, `ss`

**Helpful Reading Material:**
[Port scanner on Wikipedia](https://en.wikipedia.org/wiki/Port_scanner)

First, check which ports are open on localhost with the `nmap` tool.

```bash
nmap -sV -p 31000-32000 localhost
```

```
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00018s latency).
Other addresses for localhost (not scanned): ::1
Not shown: 996 closed tcp ports (conn-refused)
PORT      STATE SERVICE     VERSION
31046/tcp open  echo
31518/tcp open  ssl/echo
31691/tcp open  echo
31790/tcp open  ssl/unknown
31960/tcp open  echo
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port31790-TCP:V=7.98%T=SSL%I=7%D=11/12%Time=6AF58313%P=x86_64-pc-linux-
SF:gnu%r(GenericLines,32,"Wrong!\x20Please\x20enter\x20the\x20correct\x20c
SF:urrent\x20password\.\n")%r(GetRequest,32,"Wrong!\x20Please\x20enter\x20
SF:the\x20correct\x20current\x20password\.\n")%r(HTTPOptions,32,"Wrong!\x2
SF:0Please\x20enter\x20the\x20correct\x20current\x20password\.\n")%r(RTSPR
SF:equest,32,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\x20pa
SF:ssword\.\n")%r(Help,32,"Wrong!\x20Please\x20enter\x20the\x20correct\x20
SF:current\x20password\.\n")%r(FourOhFourRequest,32,"Wrong!\x20Please\x20e
SF:nter\x20the\x20correct\x20current\x20password\.\n")%r(LPDString,32,"Wro
SF:ng!\x20Please\x20enter\x20the\x20correct\x20current\x20password\.\n")%r
SF:(SIPOptions,32,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\
SF:x20password\.\n");

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 122.69 seconds
```

Based on the `nmap` scan results, we should try to connect with `openssl` to ports 31518 and 31790 until we find the credentials for the next level.

```bash
echo "kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V" | openssl s_client -connect localhost:31518 -ign_eof
```

```
Connecting to 127.0.0.1
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN=SnakeOil
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN=SnakeOil
verify return:1
---
Certificate chain
 0 s:CN=SnakeOil
   i:CN=SnakeOil
   a:PKEY: RSA, 4096 (bit); sigalg: sha256WithRSAEncryption
   v:NotBefore: Jun 10 03:59:50 2024 GMT; NotAfter: Jun  8 03:59:50 2034 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIFBzCCAu+gAwIBAgIUBLz7DBxA0IfojaL/WaJzE6Sbz7cwDQYJKoZIhvcNAQEL
BQAwEzERMA8GA1UEAwwIU25ha2VPaWwwHhcNMjQwNjEwMDM1OTUwWhcNMzQwNjA4
MDM1OTUwWjATMREwDwYDVQQDDAhTbmFrZU9pbDCCAiIwDQYJKoZIhvcNAQEBBQAD
ggIPADCCAgoCggIBANI+P5QXm9Bj21FIPsQqbqZRb5XmSZZJYaam7EIJ16Fxedf+
jXAv4d/FVqiEM4BuSNsNMeBMx2Gq0lAfN33h+RMTjRoMb8yBsZsC063MLfXCk4p+
09gtGP7BS6Iy5XdmfY/fPHvA3JDEScdlDDmd6Lsbdwhv93Q8M6POVO9sv4HuS4t/
jEjr+NhE+Bjr/wDbyg7GL71BP1WPZpQnRE4OzoSrt5+bZVLvODWUFwinB0fLaGRk
GmI0r5EUOUd7HpYyoIQbiNlePGfPpHRKnmdXTTEZEoxeWWAaM1VhPGqfrB/Pnca+
vAJX7iBOb3kHinmfVOScsG/YAUR94wSELeY+UlEWJaELVUntrJ5HeRDiTChiVQ++
wnnjNbepaW6shopybUF3XXfhIb4NvwLWpvoKFXVtcVjlOujF0snVvpE+MRT0wacy
tHtjZs7Ao7GYxDz6H8AdBLKJW67uQon37a4MI260ADFMS+2vEAbNSFP+f6ii5mrB
18cY64ZaF6oU8bjGK7BArDx56bRc3WFyuBIGWAFHEuB948BcshXY7baf5jjzPmgz
mq1zdRthQB31MOM2ii6vuTkheAvKfFf+llH4M9SnES4NSF2hj9NnHga9V08wfhYc
x0W6qu+S8HUdVF+V23yTvUNgz4Q+UoGs4sHSDEsIBFqNvInnpUmtNgcR2L5PAgMB
AAGjUzBRMB0GA1UdDgQWBBTPo8kfze4P9EgxNuyk7+xDGFtAYzAfBgNVHSMEGDAW
gBTPo8kfze4P9EgxNuyk7+xDGFtAYzAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3
DQEBCwUAA4ICAQAKHomtmcGqyiLnhziLe97Mq2+Sul5QgYVwfx/KYOXxv2T8ZmcR
Ae9XFhZT4jsAOUDK1OXx9aZgDGJHJLNEVTe9zWv1ONFfNxEBxQgP7hhmDBWdtj6d
taqEW/Jp06X+08BtnYK9NZsvDg2YRcvOHConeMjwvEL7tQK0m+GVyQfLYg6jnrhx
egH+abucTKxabFcWSE+Vk0uJYMqcbXvB4WNKz9vj4V5Hn7/DN4xIjFko+nREw6Oa
/AUFjNnO/FPjap+d68H1LdzMH3PSs+yjGid+6Zx9FCnt9qZydW13Miqg3nDnODXw
+Z682mQFjVlGPCA5ZOQbyMKY4tNazG2n8qy2famQT3+jF8Lb6a4NGbnpeWnLMkIu
jWLWIkA9MlbdNXuajiPNVyYIK9gdoBzbfaKwoOfSsLxEqlf8rio1GGcEV5Hlz5S2
txwI0xdW9MWeGWoiLbZSbRJH4TIBFFtoBG0LoEJi0C+UPwS8CDngJB4TyrZqEld3
rH87W+Et1t/Nepoc/Eoaux9PFp5VPXP+qwQGmhir/hv7OsgBhrkYuhkjxZ8+1uk7
tUWC/XM0mpLoxsq6vVl3AJaJe1ivdA9xLytsuG4iv02Juc593HXYR8yOpow0Eq2T
U5EyeuFg5RXYwAPi7ykw1PW7zAPL4MlonEVz+QXOSx6eyhimp1VZC11SCg==
-----END CERTIFICATE-----
subject=CN=SnakeOil
issuer=CN=SnakeOil
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: rsa_pss_rsae_sha256
Negotiated TLS1.3 group: X25519MLKEM768
---
SSL handshake has read 3191 bytes and written 1613 bytes
Verification error: self-signed certificate
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Protocol: TLSv1.3
Server public key is 4096 bit
This TLS version forbids renegotiation.
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 18 (self-signed certificate)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: E6835DD711E5EB02D8482C5D561F277D671CB5ADDDA53B96611A49F409B01938
    Session-ID-ctx: 
    Resumption PSK: 913D4DDDFC82EF94A260A338C9CFDEDBCF56A1CF355D876B9DE13ADBE61F1B1BA9BF62BD99A9AFFBEF0F899BDD66E150
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 41 37 85 3c 49 ef 55 2e-4b 05 58 eb 5d 8b 84 cc   A7.<I.U.K.X.]...
    0010 - 25 f0 7c ca a4 8b c2 01-22 0c 6a d5 be 4b e0 5e   %.|.....".j..K.^
    0020 - 3b 62 93 b6 86 1e e5 a6-07 f9 e1 14 99 24 4c 09   ;b...........$L.
    0030 - 52 a7 fa 48 a8 05 ba 49-c5 30 7e 15 2c 50 32 25   R..H...I.0~.,P2%
    0040 - 89 7b 1b d4 3b 65 c5 ae-a5 ea 0a 12 02 45 1e 3f   .{..;e.......E.?
    0050 - ef a8 e1 a4 bf 32 d5 a4-90 75 7b 63 88 a6 9d 8c   .....2...u{c....
    0060 - 0a 60 f4 ab 28 0e 9b 0d-d5 62 4e d2 8c 58 39 66   .`..(....bN..X9f
    0070 - 32 35 a7 f6 41 eb fa d9-96 8c d9 37 79 d5 ac 50   25..A......7y..P
    0080 - 95 f0 ed 1c e4 5b 2c 01-51 1a e8 ff c3 6c 9e 8e   .....[,.Q....l..
    0090 - 21 9b 91 93 26 05 4f 20-3f bb d4 bd ad 38 6b 44   !...&.O ?....8kD
    00a0 - 8f eb 95 7d 6a 3d ce a5-77 ce 35 be c7 44 89 bf   ...}j=..w.5..D..
    00b0 - 21 c6 e9 0b 90 2c 5c 17-e7 64 f3 21 8d ea fd f6   !....,\..d.!....
    00c0 - 65 0e c8 d6 e8 cc 00 64-5c b1 dd 64 06 1a ef 82   e......d\..d....
    00d0 - 47 45 b9 59 ff 06 bb 19-cc aa 83 58 e8 4e a8 22   GE.Y.......X.N."

    Start Time: 1794474967
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 3166518494C46FB1C9E37B37E64A813E6B0B239083F1A6EBA182A43410D6FB52
    Session-ID-ctx: 
    Resumption PSK: B4568DAF5DDBD3E8B19731B548500C632FBAB4BE97AD6A5BA2A69C5541E879BBB467D12270365032678856A216B6692C
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 41 37 85 3c 49 ef 55 2e-4b 05 58 eb 5d 8b 84 cc   A7.<I.U.K.X.]...
    0010 - ea 82 38 85 57 12 67 6f-47 4e a8 92 db 3c 54 8e   ..8.W.goGN...<T.
    0020 - 97 1f 05 73 7d 76 d5 ef-01 57 a3 c9 7e 88 71 3d   ...s}v...W..~.q=
    0030 - 09 b4 1f 72 9f b3 47 7b-9e c7 ef 64 51 52 21 3f   ...r..G{...dQR!?
    0040 - eb 5c 20 4c b2 53 ae b8-b9 85 a1 af eb ac 15 e4   .\ L.S..........
    0050 - 7c 98 f5 bc fe 81 ad 2c-9a 5b 04 65 40 f2 04 f8   |......,.[.e@...
    0060 - 1b 34 3e 30 bb 70 b8 48-2e ba a6 b5 92 9a d9 c8   .4>0.p.H........
    0070 - 12 d6 b0 04 36 5e 46 34-9a 47 e6 92 f3 7a a2 60   ....6^F4.G...z.`
    0080 - dd 58 90 be e1 09 ee 02-74 d4 08 fd 64 a2 c1 08   .X......t...d...
    0090 - a8 5e 6c b9 e7 16 1e 56-a5 f4 f7 1d aa 41 0a 94   .^l....V.....A..
    00a0 - 77 5d ef 8d ce 93 56 02-95 4d 31 ca 6e 3a 96 8f   w]....V..M1.n:..
    00b0 - e0 01 15 15 e9 9c 48 68-b1 09 66 91 4f 31 87 26   ......Hh..f.O1.&
    00c0 - 9e bf 04 2a 6a 3f 4d b1-05 86 d6 a3 fb 89 fc 68   ...*j?M........h
    00d0 - 31 93 2d 7c 57 96 19 7f-1b 53 04 81 b5 40 c3 0e   1.-|W....S...@..

    Start Time: 1794474967
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V
closed
```

Let’s try another port.

```bash
echo "kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V" | openssl s_client -connect localhost:31790 -ign_eof
```

```
Connecting to 127.0.0.1
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN=SnakeOil
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN=SnakeOil
verify return:1
---
Certificate chain
 0 s:CN=SnakeOil
   i:CN=SnakeOil
   a:PKEY: RSA, 4096 (bit); sigalg: sha256WithRSAEncryption
   v:NotBefore: Jun 10 03:59:50 2024 GMT; NotAfter: Jun  8 03:59:50 2034 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIFBzCCAu+gAwIBAgIUBLz7DBxA0IfojaL/WaJzE6Sbz7cwDQYJKoZIhvcNAQEL
BQAwEzERMA8GA1UEAwwIU25ha2VPaWwwHhcNMjQwNjEwMDM1OTUwWhcNMzQwNjA4
MDM1OTUwWjATMREwDwYDVQQDDAhTbmFrZU9pbDCCAiIwDQYJKoZIhvcNAQEBBQAD
ggIPADCCAgoCggIBANI+P5QXm9Bj21FIPsQqbqZRb5XmSZZJYaam7EIJ16Fxedf+
jXAv4d/FVqiEM4BuSNsNMeBMx2Gq0lAfN33h+RMTjRoMb8yBsZsC063MLfXCk4p+
09gtGP7BS6Iy5XdmfY/fPHvA3JDEScdlDDmd6Lsbdwhv93Q8M6POVO9sv4HuS4t/
jEjr+NhE+Bjr/wDbyg7GL71BP1WPZpQnRE4OzoSrt5+bZVLvODWUFwinB0fLaGRk
GmI0r5EUOUd7HpYyoIQbiNlePGfPpHRKnmdXTTEZEoxeWWAaM1VhPGqfrB/Pnca+
vAJX7iBOb3kHinmfVOScsG/YAUR94wSELeY+UlEWJaELVUntrJ5HeRDiTChiVQ++
wnnjNbepaW6shopybUF3XXfhIb4NvwLWpvoKFXVtcVjlOujF0snVvpE+MRT0wacy
tHtjZs7Ao7GYxDz6H8AdBLKJW67uQon37a4MI260ADFMS+2vEAbNSFP+f6ii5mrB
18cY64ZaF6oU8bjGK7BArDx56bRc3WFyuBIGWAFHEuB948BcshXY7baf5jjzPmgz
mq1zdRthQB31MOM2ii6vuTkheAvKfFf+llH4M9SnES4NSF2hj9NnHga9V08wfhYc
x0W6qu+S8HUdVF+V23yTvUNgz4Q+UoGs4sHSDEsIBFqNvInnpUmtNgcR2L5PAgMB
AAGjUzBRMB0GA1UdDgQWBBTPo8kfze4P9EgxNuyk7+xDGFtAYzAfBgNVHSMEGDAW
gBTPo8kfze4P9EgxNuyk7+xDGFtAYzAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3
DQEBCwUAA4ICAQAKHomtmcGqyiLnhziLe97Mq2+Sul5QgYVwfx/KYOXxv2T8ZmcR
Ae9XFhZT4jsAOUDK1OXx9aZgDGJHJLNEVTe9zWv1ONFfNxEBxQgP7hhmDBWdtj6d
taqEW/Jp06X+08BtnYK9NZsvDg2YRcvOHConeMjwvEL7tQK0m+GVyQfLYg6jnrhx
egH+abucTKxabFcWSE+Vk0uJYMqcbXvB4WNKz9vj4V5Hn7/DN4xIjFko+nREw6Oa
/AUFjNnO/FPjap+d68H1LdzMH3PSs+yjGid+6Zx9FCnt9qZydW13Miqg3nDnODXw
+Z682mQFjVlGPCA5ZOQbyMKY4tNazG2n8qy2famQT3+jF8Lb6a4NGbnpeWnLMkIu
jWLWIkA9MlbdNXuajiPNVyYIK9gdoBzbfaKwoOfSsLxEqlf8rio1GGcEV5Hlz5S2
txwI0xdW9MWeGWoiLbZSbRJH4TIBFFtoBG0LoEJi0C+UPwS8CDngJB4TyrZqEld3
rH87W+Et1t/Nepoc/Eoaux9PFp5VPXP+qwQGmhir/hv7OsgBhrkYuhkjxZ8+1uk7
tUWC/XM0mpLoxsq6vVl3AJaJe1ivdA9xLytsuG4iv02Juc593HXYR8yOpow0Eq2T
U5EyeuFg5RXYwAPi7ykw1PW7zAPL4MlonEVz+QXOSx6eyhimp1VZC11SCg==
-----END CERTIFICATE-----
subject=CN=SnakeOil
issuer=CN=SnakeOil
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: rsa_pss_rsae_sha256
Negotiated TLS1.3 group: X25519MLKEM768
---
SSL handshake has read 3191 bytes and written 1613 bytes
Verification error: self-signed certificate
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Protocol: TLSv1.3
Server public key is 4096 bit
This TLS version forbids renegotiation.
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 18 (self-signed certificate)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 4F62E1DA1D77B338CEB3FA6E7CD8CC24EDBCB436F9E5FF3BAC46B66D6C02DC75
    Session-ID-ctx: 
    Resumption PSK: 0763BB302F0BEF7D9971ACABBE865AAC35DC5537C3525371A00DF87E09773CFE1A10E26261FB3DFD83D7A1B96D9903A2
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 22 95 15 fa 1f 6f d1 a2-53 f6 09 2c b9 97 83 c9   "....o..S..,....
    0010 - be 2b 93 e3 e4 fc 17 05-7f 0f f1 d2 0b eb 3c 2f   .+............</
    0020 - 71 8c 77 d3 d3 a8 0a e0-56 f8 90 02 a2 c4 30 9c   q.w.....V.....0.
    0030 - 97 93 ac 59 97 ef 07 8c-0c 5b c9 91 cc f8 fe 49   ...Y.....[.....I
    0040 - 54 4a 9f b6 79 6a 1c c0-e7 b0 f0 13 da 3e e3 7a   TJ..yj.......>.z
    0050 - 9b bd d8 0d f3 d0 9c 16-59 b7 6e 45 42 8d 70 fb   ........Y.nEB.p.
    0060 - 69 0f 33 60 58 7b 92 22-0e 14 7f 0c f9 f8 f3 bc   i.3`X{."........
    0070 - fc 95 db e1 7a 9d e0 e6-5f 6c 56 b0 7e 64 75 64   ....z..._lV.~dud
    0080 - 10 b1 48 4b d0 b5 9a 89-dd 9f 2a ea ee ad cc c4   ..HK......*.....
    0090 - 4a 4c 6d cb 83 54 1d 39-ac 2a 2c d6 71 4e b8 0b   JLm..T.9.*,.qN..
    00a0 - 0e bf 02 22 04 1a a4 21-39 49 91 8c 2a 63 02 f6   ..."...!9I..*c..
    00b0 - 2a 6f 8e e8 a9 a5 c4 a1-97 3c 2e e2 3b 9f df 8a   *o.......<..;...
    00c0 - 2b bf d2 05 f9 12 b7 60-3f 87 4b 24 19 aa 93 ad   +......`?.K$....
    00d0 - 53 4c a2 ec e8 d4 80 22-2d 3b 68 3b 6b 5a 1b 21   SL....."-;h;kZ.!

    Start Time: 1794475697
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 8DC7A6C1EA62D83A321AE2C2E7ADD512A3FBB4E705B903A890348201CD4C0EA0
    Session-ID-ctx: 
    Resumption PSK: 5FA8868D5F1437F9145BD0AA48EAC97BCBE037C0E1D4EDD10A3EDD686F3C98BFEF7A8D493A7B9D9988642E09ABA65A10
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 22 95 15 fa 1f 6f d1 a2-53 f6 09 2c b9 97 83 c9   "....o..S..,....
    0010 - 6f dc 3d a9 95 cd 1b 59-4c 40 e6 91 e9 af af fc   o.=....YL@......
    0020 - cf 2b 13 db 3c 8f 04 98-ef 21 20 0a 1d 6a 35 ac   .+..<....! ..j5.
    0030 - 1e ad c7 fc 57 02 06 d1-ed 89 51 0e c1 3e 5c 36   ....W.....Q..>\6
    0040 - f9 c0 29 a5 27 25 00 02-e9 91 06 dd 6a da e8 9f   ..).'%......j...
    0050 - 27 8d ed 2c 60 cb 29 62-38 9e 41 48 e6 55 d6 de   '..,`.)b8.AH.U..
    0060 - 67 80 86 bb 12 b0 31 2f-51 0e 90 2e 7a 77 bb 2e   g.....1/Q...zw..
    0070 - bd f9 9c 9e 5d 5e e3 c4-32 b8 48 49 0e f6 68 4e   ....]^..2.HI..hN
    0080 - fe 79 1d 3d e8 8a 59 73-f6 0f 09 5c dd 5a db 09   .y.=..Ys...\.Z..
    0090 - cb b8 22 44 7f 61 bc 5d-9b 65 97 4e da 3b 82 4a   .."D.a.].e.N.;.J
    00a0 - 9b 38 dc 5d 8f 75 09 7a-da 48 dc 12 96 ae 24 63   .8.].u.z.H....$c
    00b0 - 91 d3 5c 0d 94 38 18 f9-3e 68 61 b5 04 50 38 1c   ..\..8..>ha..P8.
    00c0 - 2f f5 fd cf 38 4c 0f 8f-f0 f3 db 3d 11 28 bf dd   /...8L.....=.(..
    00d0 - 3f ef 27 1f ba 0a ba 72-31 94 b5 80 8e 61 3f a1   ?.'....r1....a?.

    Start Time: 1794475697
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
Correct!
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAABlwAAAAdzc2gtcn
NhAAAAAwEAAQAAAYEAvdSaw8j1FQ2DjtbQPGiEVtqEG5kt3g71uDlixg42vRN2MvWRVnGQ
t4k9T9tDWaisnn+6I4RCkhEzw231WA6KVc0Sd0+6/6Cp1Egp4o4l+xf5gPNo7A2OqjqN67
Hhy6I71GBjyUBnp6vEtkI3WZmZtuxpCMPyHSy7m56lipJFddKEOUCX21hNWWy2SAZQFBub
3M1hrcar5cA4pCFJ2AmjSsOP4yRbdERh3vZTGNjKe2x+ze4jf2/Y/uNdmixdaAMuD8to4Y
f7JylXL/+ohzasOYM0iNFvr8gkOOc11xuTNdbGNmu1Ff3Vp1qtJNB600EWrBt9H4xl7/WX
wEQ0/3EbpjUxGm3ZyUU5FmD4CGh1l9w4FqMD+RT9T3AVuzX8NM1FiIAkQMe0b34qF7iTjd
Tc+2Ve7Ywaakm79JYFnwirYd9QORxmjqUO+H6Yn9xLFmpRkFjvVf3NfvekRtV5Fm7le9wr
ipXljZ1hkHfH6echM3pINiJJHiZAgB/CDPVRdLhtAAAFiPHONUjxzjVIAAAAB3NzaC1yc2
EAAAGBAL3UmsPI9RUNg47W0DxohFbahBuZLd4O9bg5YsYONr0TdjL1kVZxkLeJPU/bQ1mo
rJ5/uiOEQpIRM8Nt9VgOilXNEndPuv+gqdRIKeKOJfsX+YDzaOwNjqo6jeux4cuiO9RgY8
lAZ6erxLZCN1mZmbbsaQjD8h0su5uepYqSRXXShDlAl9tYTVlstkgGUBQbm9zNYa3Gq+XA
OKQhSdgJo0rDj+MkW3REYd72UxjYyntsfs3uI39v2P7jXZosXWgDLg/LaOGH+ycpVy//qI
c2rDmDNIjRb6/IJDjnNdcbkzXWxjZrtRX91adarSTQetNBFqwbfR+MZe/1l8BENP9xG6Y1
MRpt2clFORZg+AhodZfcOBajA/kU/U9wFbs1/DTNRYiAJEDHtG9+Khe4k43U3PtlXu2MGm
pJu/SWBZ8Iq2HfUDkcZo6lDvh+mJ/cSxZqUZBY71X9zX73pEbVeRZu5XvcK4qV5Y2dYZB3
x+nnITN6SDYiSR4mQIAfwgz1UXS4bQAAAAMBAAEAAAGACMy4N+cy5TzxIkf28zXtHJGYmi
bpp2eOIHIYkBHMm8sxKX+UsyskiD2GaBND9f4Jsnc9S7Qv2dGOUrrgKqrR4tRUzM8XXg42
kS6fMm9gd1lPKZke/gJK4L1CIvDmBKiKmXe2aHfh1jXyMnizVCX4qDAhVlSu/oc6UyZxih
Dpw2J02qqR34siWsjdUk1onOYCvaOPqZySD15vwbwBTlB0D10taFwhGSyqVMmaZIZ4LGyF
HEqzvo6Swo4Lor/3vICZJ5YLuUVa2GEEx5Ir1Np/fb3C+zKe37+HPf5lhDps2OWXNf1D/N
KhPt9QbhANoATORB+64nNw66/515vslhB7JMn4Yy/mJjJe0uR8cC4nnqXGBOy6lIFzbNQN
DastUidaMaqpswS49R5/Uq2YYOjbU+YCbBJz8qaz8eUMhlMsOI6b2XGwtr4rP9fENWrqxs
z3bYvw2I4t8G/OgZESZvn+DCTAuc/+/NtIeLDTeJJsUggkU5Xm4Xdmz1y0SwRqTRpJAAAA
wQCiE/31KZCUQJfwdZ1Ll6iXZ9ANreda++OlCkVQTGmfjnPAwpc2io/n0IkjE5Rch9bHkR
n/Pnm228x2TaWcq0FsyP9VnZQIw3LYPZxxouvV4ODFeThi6dJij9X7WnyvNVaeQam5Mqzd
6eI4L9f6p43JivvRLc7IrEDMjSXMcnlUbvEFa/143fpHZer9q+9qARUSLIodr8D6zde3l0
r88E0Z0YZrWn1BzjPZr2z+3GPTcfYPM+pLPT3OgAjd7gVr7pEAAADBAN2qsjh6rfgKHiou
n+pf1TUIXLzpnY+icwYcotvfhjweF1KwowzqnNjG0olJqc5B6O2g8FbeIn3a1v/896Ynb3
WXXYs1cCXGyyWxkw5nWaSWS8GMVEpjIgvW46hnrWmDVEPuW84wsgZ1yGnL0InHq3SmGMVe
7FLVoO2LD393RW/2RcMZ8mX/SWGLst9IunzxoEHGxJObKWv6C2IgQj8zHDpuE/6TwdDeFS
3KWM+JyggnB+EEssW7Tu+N2H+3mgLNbwAAAMEA2zuReO3x3LioX2U5O2ZmawKeajDKAUWh
OmfbD3ab8psuVcllydLWQfmJmJ7xXyAEtmO2kIg6ax6AEd4PLAgDC504v+bmLPjdvSwqGk
//vONxwDY+Uy3m3oX+MHK2KRq5Zd3YJd9Px6AF5iMbyiQYA69nsBumqt04Ihe8CFYHa9uG
KLE1QobuX5Wx6cWaOsc1j61vpaYDEwMUT8LeMFqKjN1rF1LMiNENBQhtd+ikJmYYwB01/5
Pfos/2C+rbNuHjAAAADnJ1ZHlAbG9jYWxob3N0AQIDBA==
-----END OPENSSH PRIVATE KEY-----

closed
```

Let’s copy the OpenSSH private key into a new file on the local Linux machine.

```bash
nano /Desktop/bandit17.key
```

Paste the private key into `bandit17.key`.

Then, change the permissions of `bandit17.key`.

```bash
chmod 600 /Desktop/bandit17.key
```

Finally, connect to the SSH server using that private key.

```bash
ssh -i /Desktop/bandit17.key bandit17@bandit.labs.overthewire.org -p 2220 
```

To get the password for `bandit17`, read `/etc/bandit_pass/bandit17`.

```bash
cat /etc/bandit_pass/bandit17
```

```
pWXMAZoxGC8JmDMfmT5MGEsobMM3vnj2
```

> 🔑 **Password (Level 17):** `pWXMAZoxGC8JmDMfmT5MGEsobMM3vnj2`

---

# Level 17 → Level 18

**Level Goal:** There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**

**Commands you may need to solve this level:**

`cat`, `grep`, `ls`, `diff`

To compare the files, use `diff`.

```bash
diff passwords.old passwords.new
```

```
42c42
< 1WJHmb0k7TH4piWp9Pd0lsruErLQZrR9
---
> OQxXZjELndr90zuhOTDYBEomI0SZITXI
```

From this result, the changed line is `OQxXZjELndr90zuhOTDYBEomI0SZITXI`, and it is the password for `bandit18`.

> 🔑 **Password (Level 18):** `OQxXZjELndr90zuhOTDYBEomI0SZITXI`

---

# Level 18 → Level 19

**Level Goal:** The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.

**Commands you may need to solve this level:**

`ssh`, `ls`, `cat`

When we try to log in with `ssh`, the connection closes immediately.

To view the `readme` file, we pass the command to run directly in the `ssh` command:

```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```

```
KpsOfPkcP7i1FlIExk2QEjyt6dw8dxZI
```

> 🔑 **Password (Level 19):** `KpsOfPkcP7i1FlIExk2QEjyt6dw8dxZI`

---

# Level 19 → Level 20

**Level Goal:** To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

**Helpful Reading Material:**
[setuid on Wikipedia](https://en.wikipedia.org/wiki/Setuid)

First, let's check the contents and permissions of the files in the home directory using `ls -la`:

```bash
ls -la
```

```
total 36
drwxr-xr-x   2 root     root      4096 Oct 25 13:37 .
drwxr-xr-x 150 root     root      4096 Oct 25 13:40 ..
-rw-r--r--   1 root     root       220 Feb 13  2026 .bash_logout
-rw-r--r--   1 root     root      3851 Oct 25 13:21 .bashrc
-rw-r--r--   1 root     root       807 Feb 13  2026 .profile
-rwsr-x---   1 bandit20 bandit19 14880 Oct 25 13:37 bandit20-do
```

Looking at the permissions of `bandit20-do` (`-rwsr-x---`), we can see the **SUID (Set User ID)** bit (`s`) is set, and the file is owned by `bandit20`. **SUID Bit (`s`):** A special permission in Linux that allows a user to execute a file with the permissions of the file's owner rather than the user running it. This means when `bandit19` executes this binary, it runs with the privileges of `bandit20`.

Let's run the binary without any arguments to see its usage instructions:

```bash
./bandit20-do
```

```
Run a command as another user. Example: ./bandit20-do id
```

Since `bandit20-do` executes commands as `bandit20`, we can use `cat` through this binary to read the password file for `bandit20`:

```bash
./bandit20-do cat /etc/bandit_pass/bandit20
```

```bash
4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA
```

> 🔑 **Password (Level 20):** `4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA`

---

# Level 20 → Level 21

**Level Goal:** There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE: Try connecting to your own network daemon to see if it works as you think**

**Commands you may need to solve this level:**
`ssh`, `nc`, `cat`, `bash`, `screen`, `tmux`, Unix ‘job control’ (`bg`, `fg`, `jobs`, `&`, `CTRL-Z`, …)

```bash
ls -la
```

```
total 36
drwxr-xr-x   2 root     root      4096 Oct 25 13:37 .
drwxr-xr-x 150 root     root      4096 Oct 25 13:40 ..
-rw-r--r--   1 root     root       220 Feb 13  2026 .bash_logout
-rw-r--r--   1 root     root      3851 Oct 25 13:21 .bashrc
-rw-r--r--   1 root     root       807 Feb 13  2026 .profile
-rwsr-x---   1 bandit21 bandit20 15604 Oct 25 13:37 suconnect
```

To solve this level, we need to set up a local listener on an arbitrary available port, connect the `suconnect` binary to that port, and send the current level's password over the connection.

#### Terminal 1

**1. Start a Netcat Listener (Terminal 1)**

Open an SSH session as `bandit20` and start listening on an unused port (e.g., `39482`) using `nc` (Netcat):

```bash
nc -l -p 39482
```

**3. Send the Password & Retrieve the Next One**

Back in **Terminal 1**, paste the password for `bandit20` and press **Enter**.

```
4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA
```

**5. Response**

The `suconnect` binary sends back the password for `bandit21`.

```
bW9kBv5WC3P4yoDyf12LSdGuNz5ka6hY
```

#### Terminal 2

**2. Connect Using the Setuid Binary (Terminal 2)**

Open a second SSH session as `bandit20` and run the `suconnect` binary pointing to the listening port:

```bash
./suconnect 39482
```

**4. Checking**

`suconnect` will verify the password:

```
Read: 4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA
Password matches, sending next password
```

> 🔑 **Password (Level 21):** `bW9kBv5WC3P4yoDyf12LSdGuNz5ka6hY`

---

# Level 21 → Level 22

**Level Goal:** A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.
****

**Commands you may need to solve this level:**

`cron`, `crontab`, `crontab(5)` (use “man 5 crontab” to access this)

```bash
cd /etc/cron.d/
ls -la
```

```
total 56
drwxr-xr-x   2 root root  4096 Oct 26 15:53 .
drwxr-xr-x 128 root root 12288 Oct 26 15:53 ..
-rw-r--r--   1 root root   102 Nov  5  2025 .placeholder
-r--r-----   1 root root    47 Oct 25 13:37 behemoth4_cleanup
-rw-r--r--   1 root root   127 Oct 26 15:53 clean_tmp
-rw-r--r--   1 root root   120 Oct 25 13:37 cronjob_bandit22
-rw-r--r--   1 root root   122 Oct 25 13:37 cronjob_bandit23
-rw-r--r--   1 root root   120 Oct 25 13:37 cronjob_bandit24
-rw-r--r--   1 root root   188 Feb 13  2026 e2scrub_all
-r--r-----   1 root root    48 Oct 25 13:39 leviathan5_cleanup
-rw-------   1 root root   138 Oct 25 13:39 manpage3_resetpw_job
-rwx------   1 root root    52 Oct 25 13:41 otw-tmp-dir
```

We need to analyze `cronjob_bandit22`.

```bash
cat cornjob_bandit22
```

```
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
```

This cron job runs `/usr/bin/cronjob_bandit22.sh`. Let’s open that file.

```bash
 cat  /usr/bin/cronjob_bandit22.sh
```

```
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```

This script reads the password of `bandit22` and writes it to `/tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv`.

```bash
 cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```

```
RYVux2rHEm9tiXHmLFzuR7Vhx6AZQMEz
```

> 🔑 **Password (Level 22):** `RYVux2rHEm9tiXHmLFzuR7Vhx6AZQMEz`

---

# Level 22 → Level 23

**Level Goal:** A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

**Commands you may need to solve this level:**

`cron`, `crontab`, `crontab(5)` (use “man 5 crontab” to access this)

```bash
cd /etc/cron.d/
ls -la
```

```
total 56
drwxr-xr-x   2 root root  4096 Oct 26 15:53 .
drwxr-xr-x 128 root root 12288 Oct 26 15:53 ..
-rw-r--r--   1 root root   102 Nov  5  2025 .placeholder
-r--r-----   1 root root    47 Oct 25 13:37 behemoth4_cleanup
-rw-r--r--   1 root root   127 Oct 26 15:53 clean_tmp
-rw-r--r--   1 root root   120 Oct 25 13:37 cronjob_bandit22
-rw-r--r--   1 root root   122 Oct 25 13:37 cronjob_bandit23
-rw-r--r--   1 root root   120 Oct 25 13:37 cronjob_bandit24
-rw-r--r--   1 root root   188 Feb 13  2026 e2scrub_all
-r--r-----   1 root root    48 Oct 25 13:39 leviathan5_cleanup
-rw-------   1 root root   138 Oct 25 13:39 manpage3_resetpw_job
-rwx------   1 root root    52 Oct 25 13:41 otw-tmp-dir
```

Do the same steps as before.

```bash
cat cronjob_bandit23
```

```
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
```

```bash
cat /usr/bin/cronjob_bandit23.sh
```

```
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
```

Let’s define `myname` and `mytarget`:

```bash
whoami
```

```
bandit23
```

`myname` = `bandit23`

```bash
echo I am user bandit23 | md5sum | cut -d ' ' -f 1
```

```
8ca319486bfbbc3663ea0fbe81326349
```

`mytarget` = `8ca319486bfbbc3663ea0fbe81326349`

```bash
cat /tmp/8ca319486bfbbc3663ea0fbe81326349
```

```
gKXDTAXnIz3OBxiPjRZ2uqutUlPZrBsw
```

> 🔑 **Password (Level 23):** `gKXDTAXnIz3OBxiPjRZ2uqutUlPZrBsw`

---

# Level 23 → Level 24

**Level Goal:** A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

**Commands you may need to solve this level:**

`chmod`, `cron`, `crontab`, `crontab(5)` (use “man 5 crontab” to access this)

```bash
cd /etc/cron.d/
ls -la
```

```
total 56
drwxr-xr-x   2 root root  4096 Oct 26 15:53 .
drwxr-xr-x 128 root root 12288 Oct 26 15:53 ..
-rw-r--r--   1 root root   102 Nov  5  2025 .placeholder
-r--r-----   1 root root    47 Oct 25 13:37 behemoth4_cleanup
-rw-r--r--   1 root root   127 Oct 26 15:53 clean_tmp
-rw-r--r--   1 root root   120 Oct 25 13:37 cronjob_bandit22
-rw-r--r--   1 root root   122 Oct 25 13:37 cronjob_bandit23
-rw-r--r--   1 root root   120 Oct 25 13:37 cronjob_bandit24
-rw-r--r--   1 root root   188 Feb 13  2026 e2scrub_all
-r--r-----   1 root root    48 Oct 25 13:39 leviathan5_cleanup
-rw-------   1 root root   138 Oct 25 13:39 manpage3_resetpw_job
-rwx------   1 root root    52 Oct 25 13:41 otw-tmp-dir
```

Do the same steps as before.

```bash
cat cronjob_bandit24
```

```
@reboot bandit23 /usr/bin/cronjob_bandit24.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit24.sh  &> /dev/null
```

```bash
cat /usr/bin/cronjob_bandit24.sh
```

```
#!/bin/bash

shopt -s nullglob

myname=$(whoami)

cd /var/spool/"$myname"/foo || exit
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." ] && [ "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" "./$i")"
        if [ "${owner}" = "bandit23" ] && [ -f "$i" ]; then
            timeout -s 9 60 "./$i"
        fi
        rm -rf "./$i"
    fi
```

- It sets `$myname` to `bandit24` and changes the directory to `/var/spool/bandit24/foo`.
- It loops through all files in that directory.
- If a file is owned by `bandit23`, it executes the script **as `bandit24`** (with a 60-second timeout) and then deletes it.

Since `bandit24` executes any script owned by `bandit23` inside `/var/spool/bandit24/foo`, we can write a script that reads `/etc/bandit_pass/bandit24` and outputs it to a directory we control.

First, create a temporary directory in `/tmp` and grant full permissions (`777`) so `bandit24` can write the output file inside it:

```bash
mkdir /tmp/mytemp24
cd /tmp/mytemp24
chmod 777 /tmp/mytemp24
```

Next, create the payload script `getpass.sh`:

```bash
nano getpass.sh
```

Add the following content inside `nano`, save (`Ctrl + O`, `Enter`), and exit (`Ctrl + X`):

```
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/mytemp24/pass.txt
```

Verify the contents of the script:

```bash
cat getpass.sh
```

Make the script executable and copy it into the target directory:

```bash
chmod +x getpass.sh
cp getpass.sh /var/spool/bandit24/foo/
```

Wait approximately 1 minute for the cronjob to execute and delete our script, then read the generated `pass.txt` file:

```bash
cat /tmp/mytemp24/pass.txt
```

```
hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv
```

> 🔑 **Password (Level 24):** `hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv`

---

# Level 24 → Level 25

**Level Goal:** A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing. You do not need to create new connections each time

```bash
mkdir /tmp/mybandit24
cd /tmp/mybandit24
```

```bash
touch script.sh
nano script.sh
```

```
#!/bin/bash

pass=$(cat /etc/bandit_pass/bandit24)

for i in {0000..9999}
do
    echo "$pass $i"
done | nc localhost 30002
```

```bash
chmod +x script.sh
./script.sh
```

When I executed this code, `netcat` returned:

```
Wrong! Please enter the correct current password and pincode. Try again.
```

That’s why I had to make some changes in `script.sh`.

```bash
nano script.sh
```

```
#!/bin/bash

pass=$(cat /etc/bandit_pass/bandit24)

for i in {0000..9999}
do
    echo "$pass $i"
done | nc localhost 30002 | grep -v "Wrong!"
```

```
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Correct!
The password of user bandit25 is SoHfqMOEqIX2IYKVciZxvgpR9a2Djx4P
```

> 🔑 **Password (Level 25):** `SoHfqMOEqIX2IYKVciZxvgpR9a2Djx4P`

---

# Level 25 → Level 26

**Level Goal:**  Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.

> NOTE: if you’re a Windows user and typically use Powershell to `ssh` into bandit: Powershell is known to cause issues with the intended solution to this level. You should use command prompt instead.
>

**Commands you may need to solve this level:**

`ssh`, `cat`, `more`, `vi`, `ls`, `id`, `pwd`

First, let’s check which shell is used for `bandit26`:

```bash
grep 'bandit26' /etc/passwd
```

```
bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
```

```bash
cat /usr/bin/showtext
```

```
#!/bin/sh

export TERM=linux

exec more ~/text.txt
exit 0
```

Then let’s analyze the home directory:

```bash
ls -la
```

```
total 40
drwxr-xr-x   2 root     root     4096 Oct 25 13:37 .
drwxr-xr-x 150 root     root     4096 Oct 25 13:40 ..
-rw-r-----   1 bandit25 bandit25   33 Oct 25 13:37 .bandit24.password
-rw-r-----   1 bandit25 bandit25  151 Oct 25 13:37 .banner
-rw-r--r--   1 root     root      220 Feb 13  2026 .bash_logout
-rw-r--r--   1 root     root     3851 Oct 25 13:21 .bashrc
-rw-r-----   1 bandit25 bandit25   66 Oct 25 13:37 .flag
-rw-r-----   1 bandit25 bandit25    4 Oct 25 13:37 .pin
-rw-r--r--   1 root     root      807 Feb 13  2026 .profile
-r--------   1 bandit25 bandit25 2602 Oct 25 13:37 bandit26.sshkey
```

```bash
cat bandit26.sshkey
```

```
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAABlwAAAAdzc2gtcn
NhAAAAAwEAAQAAAYEAnaAnMX2t9hzZCs5DGxtAm+ul93mVDbs8d4kmrcIblIqUd/Xl2Ain
Q2Lo8eHrG+z40alkwkUBigyS+WCUgTzLoSiYqN56Xc7fdqWCyWrHkWajejNtm0b3x0bHc/
0lGzq/AtD64DHoHy9HEZ8BLUaF+0ZBguX9pdEXz05B4hFOyC1TuCUYvxgH+jL4ZlxJ8CN0
Dj/1Sef+GBegTPjBXOHzulK4XM35M6tUvmC95Zyx8v6hsxTLSsJLny4RG2+jl9zRgZiHds
O+Pi0EPPqrP/qzSOz6+0noC/dKTTiKOXur3AJdqjZM8bEStdmuG79XRjqCv1YKVV82fMEy
+wP9QkFtMbNvx7XFdJuXY8ST1Au3E40WIeGS2X6cQHhhPZzBtqxSSF4fSQl3VtAso9LVTj
nTZtAFIL9tPImb9U+BKdJsgw3HeSs1MmTzrXI81ejp6VliL1rktywUlPr8a6kH6A14a1JJ
en4ug+KUi3/UYvCPVzXjmdXB0Gd7x1Wnkq4m/4fPAAAFiAqgp+4KoKfuAAAAB3NzaC1yc2
EAAAGBAJ2gJzF9rfYc2QrOQxsbQJvrpfd5lQ27PHeJJq3CG5SKlHf15dgIp0Ni6PHh6xvs
+NGpZMJFAYoMkvlglIE8y6EomKjeel3O33algslqx5Fmo3ozbZtG98dGx3P9JRs6vwLQ+u
Ax6B8vRxGfAS1GhftGQYLl/aXRF89OQeIRTsgtU7glGL8YB/oy+GZcSfAjdA4/9Unn/hgX
oEz4wVzh87pSuFzN+TOrVL5gveWcsfL+obMUy0rCS58uERtvo5fc0YGYh3bDvj4tBDz6qz
/6s0js+vtJ6Av3Sk04ijl7q9wCXao2TPGxErXZrhu/V0Y6gr9WClVfNnzBMvsD/UJBbTGz
b8e1xXSbl2PEk9QLtxONFiHhktl+nEB4YT2cwbasUkheH0kJd1bQLKPS1U4502bQBSC/bT
yJm/VPgSnSbIMNx3krNTJk861yPNXo6elZYi9a5LcsFJT6/GupB+gNeGtSSXp+LoPilIt/
1GLwj1c145nVwdBne8dVp5KuJv+HzwAAAAMBAAEAAAGABjaoQpPAAX+lDFra23z5PnVflz
Jg5To/IIcriN8Xrzvk9mEM0Ufc5u8g7n7jFAGXZoNC7Poe07Leny35LKp02jBW6xXMV1nA
4edMWkDSvkNuFk32ZdkoCik/iUAcOTTZWHTKLu1tR1H+WqCc09XI/t0H1u9o4NotyPSHoz
ADeU0wHfPmH4tyZQ5+dDzN9DMfSumnF/fgC7+nPyqoS4YsrNZ3E78tH6YDDlK3qaF4zbvz
4rK+kxD/9GyyvsvXPVlIskHpJvWnhVa7vzk0EAZ02P4f0FSBImDZ5NUnF1T+h3eLQlj2XM
BgzJAsLg4o/DAj/3yQtbcXhKIeq2dLc0cJwHz1e/t7BFC1GjwxXVOVVsw5aKJJOZmgHKpn
Kc393JQIMnzDS4HTIoa4DZSnX00q7MemRdPQV3rCHlwsIywSW5CrM6eR0xsphhK3WEpkV5
rU3zkidT0z2Efi1Qs3E2fIuH3okmWN8gZ6zWAgBJHJMlfl/ij3s44vdt3VSKcpUMKBAAAA
wQCrI/HTiT0XanBM9cAwvnv9wUBeCeLbUJa/r7LOQu8QrrNu9Y/6KUy9gfEEP1saHOiRNN
LNtxPpcKxYOGqZwrSzAP793raGg7Q3/OIghLPgJaRpfGlS4swxrvqG/ddG4E6+mY8BoRWy
VjFW5pKxwGCPwpkLvvPOA/0ukC1O1Spc6v1wwSvKcPKBhEQZ6fUtpWLdTn7mKaTHXhVLHv
WOTyJ8cg3fI36/UkagsiCFUoRamzY6OwZTSeS/X2SGkEvjsBYAAADBAMl3Rzmw4c/l5AjC
bmKlW/EVDTzeLe4UGePd4PMoJu1YoC8u3sKzv/rbz8vt6tHlwUsvI5NubwJ1pUaIEcL/br
FbAvkuV9NYUQqMW0qsgecXmQV2MBhZbKwLl8hq9shav6YL4RAjFIl3Xsx9ngH6BHXx51zI
2LUZXq1EZtw6wdc9glt14/w4m+N+5WRaT641O19o8yKhAHYqnwSTNUOFL8X4gkUCTQbTne
Ochzn4Q56gP2boTN2frB8hbY3j1BLMHwAAAMEAyErttPP7OJnNrYdbQ3YKVOM69o+YXa0y
5/K0uLMWTHRbKaMw6m29QuhkAh+pJlxTL5SQWVFfM84V9nvOlxOhOxukJiUdIUMFZD8OM2
Deak7ZqfRnLrbwGmBKM585fZ4qa+xP3MYhl6ckuvNUsMLX+kub5F9Ka7mUbd48LEbEsqX6
9lzWEiznRDxqrl6io92M0O90mdfPkiDcF9WZP68Apg2DOqcNMBA9kHA3HvA//Kbva0JEFg
piuGIiYum5tM5RAAAADnJ1ZHlAbG9jYWxob3N0AQIDBA==
-----END OPENSSH PRIVATE KEY-----
```

On the host OS (my local machine), create a new empty file:

```bash
touch bandit26.key
```

```bash
scp -P 2220 bandit25@bandit.labs.overthewire.org:bandit26.sshkey ./bandit26.key
```

Then try to connect to `bandit26`:

```
ssh -i bandit26.key bandit26@bandit.labs.overthewire.org -p 2220
```

But first, shrink your terminal window to only 3 or 4 lines in height.

When `--More--` appears on the screen, press `v` to open the `vim` editor. Then set `bash` as the `shell`.

```
:set shell=/bin/bash
:shell
```

Then the `bandit26@bandit:~$` prompt appears on the screen.

```bash
cat /etc/bandit_pass/bandit26
```

```
jHdv2ELQhT22BkprMNDjybZDAkw1zeBJ
```

> 🔑 **Password (Level 26):** `jHdv2ELQhT22BkprMNDjybZDAkw1zeBJ`

---

# Level 26 → Level 27

**Level Goal:** Good job getting a shell! Now hurry and grab the password for bandit27!

**Commands you may need to solve this level:**

`ls`

```bash
ls -la
```

```
total 44
drwxr-xr-x   3 root     root      4096 Oct 25 13:37 .
drwxr-xr-x 150 root     root      4096 Oct 25 13:40 ..
-rw-r--r--   1 root     root       220 Feb 13  2026 .bash_logout
-rw-r--r--   1 root     root      3851 Oct 25 13:21 .bashrc
-rw-r--r--   1 root     root       807 Feb 13  2026 .profile
drwxr-xr-x   2 root     root      4096 Oct 25 13:37 .ssh
-rwsr-x---   1 bandit27 bandit26 14880 Oct 25 13:37 bandit27-do
-rw-r-----   1 bandit26 bandit26   258 Oct 25 13:37 text.txt
```

There is an executable file (`bandit27-do`).

Run this file:

```bash
./bandit27-do
```

```
Run a command as another user.
  Example: ./bandit27-do id
```

So this file lets us run a command as `bandit27`.

```bash
./bandit27-do cat /etc/bandit_pass/bandit27
```

```bash
STJLJBRRphMxKB392CT4iOr5CbzPU9ER
```

> 🔑 **Password (Level 27):** `STJLJBRRphMxKB392CT4iOr5CbzPU9ER`

---

# Level 27 → Level 28

**Level Goal:**  There is a git repository at `ssh://bandit27-git@bandit.labs.overthewire.org/home/bandit27-git/repo` via the port `2220`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.

**Commands you may need to solve this level:**

`git`

**Helpful Reading Material:**

- [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Git from the Bottom Up](https://jwiegley.github.io/git-from-the-bottom-up/)

On the local OS, clone the git repository.

```bash
git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo
```

```bash
cd repo
ls -la
```

```
total 16
drwxr-xr-x 3 RWPenT RWPenT 4096 Nov 26 21:59 .
drwxr-xr-x 3 RWPenT RWPenT 4096 Nov 26 21:59 ..
drwxr-xr-x 7 RWPenT RWPenT 4096 Nov 26 21:59 .git
-rw-r--r-- 1 RWPenT RWPenT   68 Nov 26 21:59 README
```

```bash
cat README
```

```
The password to the next level is: y8Yd2ssKcpHpud7UvOSOxwamRMzIGIeQ
```

> 🔑 **Password (Level 28):** `y8Yd2ssKcpHpud7UvOSOxwamRMzIGIeQ`

---

# Level 28 → Level 29

**Level Goal:**  There is a git repository at `ssh://bandit28-git@bandit.labs.overthewire.org/home/bandit28-git/repo` via the port `2220`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.

**Commands you may need to solve this level:**

`git`

**Helpful Reading Material:**

- [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Git from the Bottom Up](https://jwiegley.github.io/git-from-the-bottom-up/)

```bash
git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo
```

```bash
cd repo
ls -la
```

```
total 16
drwxr-xr-x 3 RWPenT RWPenT 4096 Nov 26 22:13 .
drwxr-xr-x 3 RWPenT RWPenT 4096 Nov 26 22:10 ..
drwxr-xr-x 7 RWPenT RWPenT 4096 Nov 26 22:11 .git
-rw-r--r-- 1 RWPenT RWPenT  111 Nov 26 22:11 README.md
```

```bash
cat README.md
```

```
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

```

As you can see, the password was removed. That’s why we should look at the commit history to find the old password.

```bash
git log -p
```

```
commit eaed9252bd8c2784382d3499ea2167277fc17472 (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Sun Oct 25 13:37:26 2026 +0000

    fix info leak

diff --git a/README.md b/README.md
index 42331d9..5c6457b 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials

 - username: bandit29
-- password: Em7eGtqaMySwNFjCpwzzHhLhospOcdt0
+- password: xxxxxxxxxx

commit 26663cf19bf4014c5f9dc845b9e8feef90a84660
Author: Morla Porla <morla@overthewire.org>
Date:   Sun Oct 25 13:37:26 2026 +0000

    add missing data

diff --git a/README.md b/README.md
index 7ba2d2f..42331d9 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials

 - username: bandit29
-- password: <TBD>
+- password: Em7eGtqaMySwNFjCpwzzHhLhospOcdt0

commit 40f82538831252cec29b2d3d22ec5774369a9325
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Oct 25 13:37:26 2026 +0000

    initial commit of README.md
```

> 🔑 **Password (Level 29):** `Em7eGtqaMySwNFjCpwzzHhLhospOcdt0`

---

# Level 29 → Level 30

**Level Goal:**  There is a git repository at `ssh://bandit29-git@bandit.labs.overthewire.org/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.

**Commands you may need to solve this level:**

`git`

**Helpful Reading Material:**

- [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Git from the Bottom Up](https://jwiegley.github.io/git-from-the-bottom-up/)

```bash
git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo
```

```bash
cd repo
ls -la
```

```
total 16
drwxr-xr-x 3 RWPenT RWPenT 4096 Nov 26 22:40 .
drwxr-xr-x 3 RWPenT RWPenT 4096 Nov 26 22:40 ..
drwxr-xr-x 7 RWPenT RWPenT 4096 Nov 26 22:40 .git
-rw-r--r-- 1 RWPenT RWPenT  111 Nov 26 22:40 README.md
```

```bash
cat README.md
```

```
# Bandit Notes
Some notes for level30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

```

Let’s check branches:

```bash
git branch -a
```

```
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
```

```bash
git checkout dev
```

```bash
cat README.md
```

```
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: jq9Dfg2rXsfYsWMgFuKlXhphjdH7USgX

```

> 🔑 **Password (Level 30):** `jq9Dfg2rXsfYsWMgFuKlXhphjdH7USgX`

---

# Level 30 → Level 31

**Level Goal:**  There is a git repository at `ssh://bandit30-git@bandit.labs.overthewire.org/home/bandit30-git/repo` via the port `2220`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.

**Commands you may need to solve this level:**

`git`

**Helpful Reading Material:**

- [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Git from the Bottom Up](https://jwiegley.github.io/git-from-the-bottom-up/)

```bash
git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo
```

```bash
cd repo
ls -la
```

```
total 16
drwxr-xr-x 3 RWPenT RWPenT 4096 Nov 26 22:56 .
drwxr-xr-x 3 RWPenT RWPenT 4096 Nov 26 22:56 ..
drwxr-xr-x 7 RWPenT RWPenT 4096 Nov 26 22:56 .git
-rw-r--r-- 1 RWPenT RWPenT   30 Nov 26 22:56 README.md
```

```bash
cat README.md
```

```
just an epmty file... muahaha
```

Let’s check tags:

```bash
git tag
```

```
secret
```

```bash
git show secret
```

```
82NkymblpGBYmIXG6ZQ8YldBYstHpfUf
```

> 🔑 **Password (Level 31):** `82NkymblpGBYmIXG6ZQ8YldBYstHpfUf`

---

# Level 31 → Level 32

**Level Goal:**  There is a git repository at `ssh://bandit31-git@bandit.labs.overthewire.org/home/bandit31-git/repo` via the port `2220`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.

**Commands you may need to solve this level:**

`git`

**Helpful Reading Material:**

- [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Git from the Bottom Up](https://jwiegley.github.io/git-from-the-bottom-up/)

```bash
git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo
```

```bash
cd repo
ls -la
```

```
total 20
drwxr-xr-x 3 RWPenT RWPenT 4096 Nov 26 23:17 .
drwxr-xr-x 3 RWPenT RWPenT 4096 Nov 26 23:17 ..
drwxr-xr-x 7 RWPenT RWPenT 4096 Nov 26 23:17 .git
-rw-r--r-- 1 RWPenT RWPenT    6 Nov 26 23:17 .gitignore
-rw-r--r-- 1 RWPenT RWPenT  147 Nov 26 23:17 README.md
```

```bash
cat README.md
```

```
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master
```

```bash
cat .gitignore
```

```
*.txt
```

```bash
echo "May I come in?" > key.txt
git add -f key.txt
git commit -m "add key.txt"
git push origin master
```

```
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: pWuj5jBQ6IgV0NXwiH6g1pXRF8S1YvbT
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
```

> 🔑 **Password (Level 32):** `pWuj5jBQ6IgV0NXwiH6g1pXRF8S1YvbT`

---

# Level 32 → Level 33

**Level Goal:**  After all this `git` stuff, it’s time for another escape. Good luck!

**Commands you may need to solve this level:**

`sh`, `man`

When logging in via SSH, an uppercase shell (`UPPERCASE SHELL`) is executed.

```bash
>> ls
```

```
sh: 1: LS: Permission denied
```

It converts every command we type to uppercase, so `ls` becomes `LS` and fails, because the shell is case-sensitive. That’s why we use `$0`, which expands to the name of the current shell (`/bin/sh`).

```bash
>> $0
```

```bash
$ bash
```

This launches a `bash` shell.

```bash
cat /etc/bandit_pass/bandit33
```

```
u4P2CyPOwPGLe94RdD9Uo2FxFwvnFswM
```

> 🔑 **Password (Level 33):** `u4P2CyPOwPGLe94RdD9Uo2FxFwvnFswM`

---

# Level 33 → Level 34

**At this moment, level 34 does not exist yet.**

```bash
ls -la
```

```
total 24
drwxr-xr-x   2 root     root     4096 Oct 25 13:37 .
drwxr-xr-x 150 root     root     4096 Oct 25 13:40 ..
-rw-r--r--   1 root     root      220 Feb 13  2026 .bash_logout
-rw-r--r--   1 root     root     3851 Oct 25 13:21 .bashrc
-rw-r--r--   1 root     root      807 Feb 13  2026 .profile
```

```bash
cat README.txt
```

```
Congratulations on solving the last level of this game!

At this moment, there are no more levels to play in this game. However, we are constantly working
on new levels and will most likely expand this game with more levels soon.
Keep an eye out for an announcement on our usual communication channels!
In the meantime, you could play some of our other wargames.

If you have an idea for an awesome new level, please let us know!
```
