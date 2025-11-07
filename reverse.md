# Reverse cheatsheet

## "Classic" 

Execute the binary to get the idea of what it is doing, exept if it is a malware or you know already what it is.

Then first step is to know what it is:

```bash
# To know what file it is, if it is statically linked, stripped, arch, etc.
file binary 

# To see if the strings are giving us something, if there is no clear strings it is probably obfuscated/packed
strings binary

# TODO: add detect it easy to detect unpackers
# TODO: add stringcheese for xored strings in ctf
```

Firts dynamic analyse:

```bash
# Will only work if the binary is dynamically linked
ltrace ./binary 
# Mostly to see if there is anti-debug (ptrace), unpacking (with execve for example)
strace ./binary 
```

Tools to analyse it statically:

- Ghidra
- IDA
- R2
- Rizin (fork of R2)
- Ioita (R2 GUI)
- Cutter (Rizin GUI)
- Binary Ninja

Tools to analyse it dynamically:

- GDB
- Most of the preceeding list
- Cheat Engine (analyse memory during execution)
- PINCE (equivalent of Cheat Engine for Linux)

## JAVA

Static analysis: JADX

Dynamic analysis: Frida? +? r2frida

### APK

TODO: VM android + frida +? r2frida

## Godo

Static analysis: GDRE (just search "godo reverse")

Dynamic analysis: use Cheat Engine (will probably be game hacking)

## Gameboy

Static analysis: GhidraBoy (Ghidra extension, super easy to install)

Dynamic analysis: Emulicious (Allow to view tiles, debug, memory scan like Cheat Engine)

## Interpreted languages

Most of it is debugging and rewritting the script.

### Bash

```bash
# Will debug by printing every commands being executed
bash -x script.sh
```

### Python

TODO: "decompile" PYC code 

