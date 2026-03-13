# Core components of Linux

Kernel:
-> Kernel is the lowest level of software having operating in a privilaged mode (kernel mode). And interfacing directly with the computer hardware.
-> Manages CPU scheduling, memory allocation, file system access and peripheral devices.
-> After the bootloader, kernel initializes the hardware and mounts the root file system.
-> Whenever the process requires resources, it calls the kernal with a systemcalls (syscalls)

User Space:
-> This is the memory area where the user applications and the non kernel processes run
-> The programs in the user space run in the non privilaged mode called user mode which prevents them from directly accessing the hardware.

init/systemd:
-> After the kernel finishes the booting, it starts the first user space process called init which holds the process ID 1
-> It acts as the root process, commonly called as the parent of all the other process in the userspace.
-> It manages the entire user space environment, including the daemon, mounting file systems, Managing system targets etc

# How are processes created and managed
Process creation:
-> Processes are created when the programs get executed. These are also generated via the system calls (fork(), exec() etc)
-> A parent process creates a child process, forming a tree structure.
-> OS grants resources to the new process, often inherited from the parent process.

Process Management:
-> Process Control Block (PCB): holds the vital data (PID, resources used etc) to track the execution of the process
-> Scheduling: The processes are scheduled and scheduler manages the states of the process (running, waiting etc)
-> Context switching: The OS saves the data of the current process and it moves to the prioritised process if necessary.
-> Interprocess Communication (IPC): The processes interact with each other via pipes, socket etc

# Commonly used linux commands
pwd, ls, cd, sudo su -, cat, ps, grep etc
