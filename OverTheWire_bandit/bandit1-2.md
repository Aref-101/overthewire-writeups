# Bandit 2

**Date:** 2026-06-16

**Goal:** The password for the next level is stored in a file called `-` located in the home directory

**Tried:**
```bash
cat -        # could not read
cat -- -     # same
file -- -    # fail
file ./-     # ASCII text
cat ./-      # success
```

<details>
<summary>Solution</summary>

```bash
cat ./-
```

</details>

<details>
<summary>Password</summary>

```
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

</details>

**What I learned:**
- `./` to reference files that clash with shell syntax
- `file` to identify a file's type
