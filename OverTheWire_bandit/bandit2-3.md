# Bandit 3

**Date:** 2026-06-16

**Goal:** The password for the next level is stored in a file called `spaces in this filename` located in the home directory

**Tried:**
```bash
cat "./--spaces in this filename--"     # fail
cat "--spaces in this filename--"       # fail
cat ./--spaces\ in\ this\ filename\--   
```

<details>
<summary>Solution</summary>

```bash
cat ./--spaces\ in\ this\ filename\--
```

</details>

<details>
<summary>Password</summary>

```
redacted
```

</details>

**What I learned:**
- Backslash escaping for spaces in filenames
- `./` also handles filenames starting with `--`
