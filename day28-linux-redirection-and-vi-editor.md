# Day 28 – Linux Redirection and VI Editor

## What I Did
- Studied Linux redirection operators such as:
  - `>`
  - `>>`
  - `|`

- Learned about:
  - Standard Input (`stdin`)
  - Standard Output (`stdout`)
  - Standard Error (`stderr`)

- Studied the VI text editor and its different modes  

### Command Mode Movement
Learned navigation commands such as:
- `h`
- `j`
- `k`
- `l`
- `w`
- `b`
- `^`
- `$`

### Command Mode Actions

#### Delete Operations
Studied:
- `dd`
- `3dd`
- `dw`
- `d3w`
- `d4h`

#### Change Operations
Studied:
- `cc`
- `cw`
- `c3w`
- `c5h`

#### Copy/Yank Operations
Studied:
- `yy`
- `3yy`
- `yw`
- `y$`

#### Put/Paste Operations
Studied:
- `p`
- `P`

### Searching in VI
Learned searching functionality inside the editor  

### Insert Mode Commands
Studied:
- `a`
- `A`
- `i`
- `I`
- `o`
- `O`

### Ex Mode Commands
Studied:
- `:w`
- `:w filename`
- `:w!`
- `:e filename`
- `:q`
- `:q!`

## What I Understood
- Linux uses input/output streams to manage command communication and data flow  
- Redirection operators help control how command output and errors are handled  
- VI editor is highly keyboard-driven and optimized for fast terminal-based text editing  
- Different VI modes provide different functionalities for editing and navigation  
- Efficient text editing in Linux often relies heavily on keyboard shortcuts and command combinations  

## Concepts Covered
- Redirection operators  
- Pipes  
- `stdin`, `stdout`, `stderr`  
- VI editor  
- Command mode  
- Insert mode  
- Ex mode  
- Navigation commands  
- Delete, copy, paste, and change operations  

## Key Takeaways
- Redirection and piping are powerful Linux command-line features  
- Understanding standard streams is important for Linux command execution and scripting  
- VI editor provides efficient terminal-based text editing once shortcuts become familiar  
- Linux tools become much more powerful when combined together using pipes and redirection  

## Next Step
- Learn the fundamentals of system and security logs, then begin exploring SIEM tools 
