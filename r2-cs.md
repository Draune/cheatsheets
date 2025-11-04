# R2 cheatsheet 

## CLI

- ? : help everywhere

- aaa : analyze

- eco [theme] : change or list (if none) theme

- pdf : dissassemble function

- pdc : pseudo code C (very ugly)

- pdd : decompile with r2dec plugin

- pdg : decompile with r2ghidra plugin 

- s [function] : move to function

- iz : show strings in .data section

- iI : show info of the binary like strings

- V : sisual mode

- V! : panel mode

- Vpp : visual debugger mode

- < : gives string to stdin 

- afvs/b/r : show variable from esp/ebp/registers

- afvn [new name] [old name] : rename variables

## Visual mode

- q : quit

- p : go to the next panel 

## Visual debug mode 

- p : change panel 

- s : step in 

- S : step over

- F2 : breakpoint 

- _ : go to function

## Tools 

- rabin2 -z : strings in .data section

- rax2 : convert to hexa (or the opposite)

- r2pm : package manager

- r2pm -U[U] : update [and upgrade] packages

- r2pm -ci : clean install package
