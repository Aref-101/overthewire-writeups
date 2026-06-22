# Bandit 6-7

**Date:** 2026-6-22

**Goal:** 
The password for the next level is stored somewhere on the server and has all of the following properties:

    owned by user bandit7
    owned by group bandit6
    33 bytes in size

**Tried:**
```bash
cd 
ls -la
cat #the hidden files
cd //
cd usr
find ./ -type f -size 33c
man find
find ./ -type f -size 33c -user bandit7 -group bandit6

```

<details>
<summary>Solution</summary>

```bash
find / -type f -size 33c -user bandit7 -group bandit6
```

</details>

<details>
<summary>Password</summary>

```
redacted
```

</details>

**What I learned:**
- user and group flags
- diffrence between ./ and / (./ is current directory but / is all of the 
- files from the root of the system)
