# Bandit 8-9

**Date:** 2026-6-22

**Goal:** 
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
**Tried:**
```bash
 ls -la
 man uniq
```

<details>
<summary>Solution</summary>

```bash
sort data.txt | uniq -u
```

</details>

<details>
<summary>Password</summary>

```
redacted
```

</details>

**What I learned:**
- - the u flag from uniq which show unique files
- the sort command
- | pipe command which sends the output of the last command as the input
- of the next command and it runs like a pipeline
