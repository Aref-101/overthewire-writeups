# Bandit 11-12

**Date:** 2026-09-02

**Goal:** 
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
**Tried:**
```bash
# commands here
ls -as
cat data.txt

```

<details>
<summary>Solution</summary>

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

</details>


**What I learned:**
- rot13
- usage of tr command
