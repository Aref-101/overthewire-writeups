# Bandit 5-6

**Date:** 2026-6-18

**Goal:** 
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

    human-readable
    1033 bytes in size
    not executable

**Tried:**
```bash
ls
cd
file ./*
find ./*
man find
pwd
find ./-type f
find ./ -type f -size 1033byte 
find ./ -type f -size 1033b    
```

<details>
<summary>Solution</summary>

```bash
#i used this one
find -type f -size 1033c 
#the most accurate search would be this which includes all properties
find -type f ! -executable -size 1033c

```

</details>

<details>
<summary>Password</summary>

```redacted
```

</details>

**What I learned:**
- pwd shows current working directory that we are in right now
- find -type f shows files or file -type d shows directories
- find ./ -executable or find -executable command finds executable files 
- if we add a '!' it finds the ones that are not executable
- find ./ -size100M  finds file that is 100megabytes and the indicator
- for bytes is 'c' example: find ./ -size100c #100bytes

