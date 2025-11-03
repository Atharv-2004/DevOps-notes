# Introduction to Shell Scripting  
**Date:** 3 November 2025

Shell scripting is a method of automating tasks in UNIX and Linux systems. A shell script is a file containing a sequence of commands that are executed by the shell, which acts as a command-line interpreter.

A shell script is created by making a file with a `.sh` extension, such as `hello_world.sh`. At the beginning of the script, a shebang is added to specify the interpreter, most commonly `#!/bin/bash`. The script then contains shell commands and logic used to automate tasks.

Before execution, the script must be given executable permissions using `chmod +x filename.sh`. Once permissions are set, the script can be run using `./filename.sh`.

Variables in shell scripts are defined using the syntax `VARIABLE_NAME=value`, with no spaces around the equals sign. By convention, variable names are written in uppercase, for example `USERNAME="JohnDoe"`. Variable values are accessed using the `$VARIABLE_NAME` format. User input can be taken using the `read -p "Prompt: " VARIABLE` command.

Conditional logic is implemented using the `if` statement along with condition checks written inside square brackets. File existence can be verified using the `-f` flag within a conditional. Repetitive execution of commands is handled using looping constructs such as `for` and `while`, which iterate based on sequences or conditions.

File and directory management is performed using commands like `mkdir` to create directories and `cd` to navigate between them. Files can be created using `touch` or by redirecting input using `cat > filename`.

Linux file permissions control access for users, groups, and others. Permission symbols include `r` for read, `w` for write, and `x` for execute. These permissions are modified using the `chmod` command. For more fine-grained control, Access Control Lists (ACLs) can be used instead of traditional permission settings.

Commonly used shell commands include `ls`, `pwd`, `cd`, `rm`, `cp`, and `mv`. Commands such as `rm -rf` must be used carefully, as they remove files and directories recursively without confirmation.

String manipulation and text processing are handled using utilities such as `tr`, `sed`, and `awk`. For example, converting a string to uppercase can be done using `tr`. File searching is commonly performed using the `find` command, which locates files based on criteria such as name or path.

Regular expressions are an important concept for advanced text processing in shell scripting, though they were only briefly mentioned and not covered in depth.

Shell scripts can also define functions to group reusable logic. Functions are declared using a function name followed by parentheses and a block of commands, and are executed by calling the function name. Additionally, shell scripting can be used for system administration tasks such as creating users and groups using commands like `useradd` and `groupadd`, along with setting default shells, permissions, and related configurations.
