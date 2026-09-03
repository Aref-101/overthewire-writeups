# Bandit 12-13

**Date:** 2026-09-03

**Goal:** 
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)
**Tried:**
```bash
ls 
man mkdir
man mktemp
mktemp -d
man cp
man xxd
man gzip
man tar 
man b
file
man bzip2
cat
```

<details>
<summary>Solution</summary>

```bash
#the file is a hexdump at first so fix that and then decompress until you #reach the last layer, also run the file command after each layer to specify #the type of compression.
xxd -r data.txt layer1.bin
xxd -l 32 layer1.bin
gzip -dc "filename" > "output name"
bzip2 -dc "filename" > "output name"
tar -tvf "file name"
tar -xf "file name"
```

</details>

**What I learned:**
- A hexdump is a text representation of binary data.
- The xxd command creates a hexdump: xxd binary-file
- The xxd -r option reverses a hexdump: xxd -r data1.txt recovered.bin
- The file command identifies a file’s format: file recovered.bin
- Common gzip signature: 1f 8b
- Common bzip2 signature: 42 5a 68
- Gzip data is decompressed with: gzip -dc input > output
- Bzip2 data is decompressed with: bzip2 -dc input > output
- XZ data is decompressed with: xz -dc input > output
- Each compression layer must be identified before decompression.
- A tar archive is a container that can hold multiple files.
- Tar contents can be listed with: tar -tvf archive
- A tar archive can be extracted with: tar -xf archive -C directory
- Extracted files can be checked with: find directory -type f -exec file {} - \;
- General process: hexdump → binary file → decompress each layer → extract tar archive → final files

