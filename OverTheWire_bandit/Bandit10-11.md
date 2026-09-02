# Bandit 10-11

**Date:** 2026-09-02

**Goal:** 
The password for the next level is stored in the file data.txt, which contains base64 encoded data
**Tried:**
```bash
# commands here
ls -a
man base64
```

<details>
<summary>Solution</summary>

```bash
base64 -d data.txt
```

</details>

<details>
<summary>Password</summary>

```
redacted
```

</details>

**What I learned:**
- the d flag is for decoding strings in base64
