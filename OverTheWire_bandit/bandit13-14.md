# Bandit 13-14

**Date:** 2026-09-04

**Goal:** 
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.
If you need help with this level: a hint file can be found in the home directory.
Make sure to read the error messages as they are informative.\

**Tried:**
```bash
ls -la
man ssh
man scp
cat sshkey.private
cd /.ssh
cd ~/.ssh
ssh -p 2220 -i sshkey.private bandit14@bandit.labs.overthewire.org
man chmod
```

<details>
<summary>Solution</summary>

```bash
#from your own terminal
scp -p 2220 bandit14@bandit.labs.overthewire.org:sshkey.private
mv sshkey.private ~/.ssh
chmod 600 ~/.ssh/sshkey.private
ssh -p 2220 -i sshkey.private bandit14@bandit.labs.overthewire.org
```

</details>



**What I learned:**
- how ssh key pairs work
- usage of scp
- usage of chmod 600  which gives the owner the right to modify and read 
- the file
