## DAY 6 of Devops 45 Days 
### Linux :

Linux is a family of open-source Unix-like operating systems based on the Linux kernel. It is widely used in servers, desktops, mobile devices, and embedded systems. Here are some key points about Linux:

1. **Multiuser**: Linux is a multiuser operating system, meaning it can handle multiple users simultaneously, each with their own processes, files, and permissions.

2. **Multitasking**: Linux supports multitasking, allowing multiple processes to run concurrently.

3. **File System**: Linux uses a hierarchical file system, with the root directory ("/") at the top. Common directories include `/bin` (executables), `/home` (user home directories), `/etc` (system configuration files), and `/var` (variable data).

4. **Shell**: The shell is the command-line interface that allows users to interact with the operating system. Common Linux shells include Bash (Bourne Again Shell), Zsh (Z Shell), and Tcsh (Tenex C Shell).

5. **Package Management**: Linux distributions typically use package management systems like `apt` (Advanced Package Tool) for Debian-based distributions (e.g., Ubuntu) and `yum`/`dnf` (Yellowdog Updater Modified / Dandified YUM) for RPM-based distributions (e.g., Fedora, CentOS).

### Basics of Shell Scripting:

Shell scripting is the process of writing scripts (programs) using shell commands to automate tasks or perform operations in Linux. Bash (Bourne Again Shell) is the most commonly used shell for scripting on Linux systems. Here are some basic concepts and commands in shell scripting:

1. **Shebang**: The first line of a shell script, which specifies the path to the shell interpreter. For Bash scripts, it typically looks like `#!/bin/bash`.

2. **Variables**: Variables in shell scripts are defined using `=` sign without spaces. For example:
   ```bash
   my_var="Hello, World!"
   ```

3. **Comments**: Comments in shell scripts start with `#`. They are ignored by the shell and are used for documentation. For example:
   ```bash
   # This is a comment
   ```

4. **Printing**: To print output to the terminal, you can use the `echo` command:
   ```bash
   echo "Hello, World!"
   ```

5. **Conditional Statements**: Conditional statements like `if`, `elif`, and `else` are used for decision-making in shell scripts. For example:
   ```bash
   if [ condition ]; then
       # code to execute if condition is true
   elif [ another_condition ]; then
       # code to execute if another_condition is true
   else
       # code to execute if none of the conditions are true
   fi
   ```

6. **Loops**: Loops like `for` and `while` are used to iterate over lists of items or execute commands repeatedly. For example:
   ```bash
   for i in {1..5}; do
       echo "Number: $i"
   done
   ```

7. **Functions**: Functions allow you to group commands together and reuse them throughout your script. For example:
   ```bash
   my_function() {
       echo "Hello from my function!"
   }

   # Call the function
   my_function
   ```

