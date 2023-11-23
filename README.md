# XV Quiz (CSL 3030)

Welcome to the XV Quiz for CSL 3030 - Operating Systems!



## Instructions
- Answer the multiple-choice questions by selecting the correct option.
- For theoretical questions, provide concise and accurate explanations.
- Feel free to use this quiz for self-assessment or educational purposes.

## Multiple-Choice Questions

#### Question 1: Basics
1. What is XV6?
   - a. A programming language
   - b. A Unix-like operating system
   - c. A file system
   - d. An assembly language

#### Question 2: Architecture
2. XV6 is based on which earlier operating system?
   - a. Windows
   - b. Linux
   - c. BSD
   - d. DOS

#### Question 3: File System
3. Which file system is used in XV6?
   - a. FAT32
   - b. NTFS
   - c. ext4
   - d. simple

#### Question 4: System Calls
4. How are system calls implemented in XV6?
   - a. As functions in the C standard library
   - b. As interrupts
   - c. Through the command line
   - d. As external programs

#### Question 5: Processes
5. In XV6, what is the maximum number of processes that can run simultaneously?
   - a. 128
   - b. 256
   - c. 512
   - d. 1024

#### Question 6: Shell
6. What is the name of the shell used in XV6?
   - a. Bash
   - b. Zsh
   - c. Sh
   - d. Fish

#### Question 7: Scheduling
7. How does XV6 handle process scheduling?
   - a. Round-robin scheduling
   - b. Priority-based scheduling
   - c. First-Come-First-Serve (FCFS)
   - d. Random scheduling

#### Question 8: Memory Management
8. Which memory management technique is used in XV6?
   - a. Paging
   - b. Segmentation
   - c. Virtual Memory
   - d. None of the above

#### Question 9: Interrupts
9. How are interrupts handled in XV6?
   - a. Through polling
   - b. Using hardware interrupts
   - c. Using software interrupts
   - d. Both b and c

#### Question 10: Multithreading
10. Does XV6 support multithreading?
    - a. Yes
    - b. No

#### Bonus Question:
11. Who developed XV6?
    - a. Microsoft
    - b. Google
    - c. MIT
    - d. IBM

## Theoretical Questions

#### Question 12: Process States
12. Briefly explain the different states a process can be in within the XV6 operating system.
Ans :
   1) Running: The process is currently running on the CPU.
   2) Runnable: The process is ready to execute and waiting for the CPU to be allocated to it. 
   3) Sleeping: The process is waiting for some event to occur (like I/O completion or a specific time delay) before it can continue executing. 
   4) Zombie: This state occurs when a process has completed execution, but its parent process has not yet collected its exit status. The process is essentially dead but still has an entry in the 
      process table until its parent acknowledges its termination.
   5)Embryonic State: Initial phase of process creation. OS sets up process data but hasn't started executing yet.
   6) Unused: when process is not been used or has been terminated.


#### Question 13: File System Structure
13. Describe the structure of the file system in XV6. Include the key components and their roles.
Ans :
   The XV6 file system provides Unix like files, directories, not pathnames. The key components are:
   a) Superblock: Stores metadata about the entire file system, including total size, block size, and free block information.
   b) Inodes: Structures that contain metadata about individual files, such as permissions, size, and pointers to data blocks.
   c) Data Blocks: Actual storage blocks that hold the file's content, where file data is stored.
   d) File Discriptors: The XV6 kernel uses the file descriptor as an index into a per-process table, so that every process has a private space of file descriptors starting at zero. File descriptors 
      represent data streams that can be written into or read from
   e) Directory: Special files that store mappings between file names and corresponding inode numbers, facilitating file organization and navigation within the file system.


#### Question 14: System Calls vs. Library Functions
14. Explain the difference between system calls and library functions in the context of XV6. Provide examples of each.
Ans: 
   a) System Calls are interfaces provided by the operating system to allow user programs to request services from the kernel, like file operations (open(), read(), write()), process management 
      (fork(), exec()), or memory management (brk()).
   b) Library Functions are higher-level functions provided by libraries linked to user programs, abstracting complex operations. For instance, printf() from the C standard library for formatted 
      output or memcpy() for memory copying. These functions often utilize system calls internally but operate at a higher level than system calls, providing more user-friendly interfaces for common 
      tasks.


#### Question 15: Memory Paging
15. How does memory paging work in XV6? Discuss the benefits of using paging in memory management.
Ans :
   XV6 uses 32-bit virtual addresses, resulting in a virtual address space of 4GB. xv6 uses paging to manage its memory allocations. However, xv6 does not do demand paging, so there is no concept of 
   virtual memory. So, all valid pages of a process are always allocated physical pages.
   Benefits of Paging:
   a) Paging is an easy to use algorithm for memory management.
   b) Paging does not require intervention from the programmer.
   c) Frames don't need to be contiguous.
   d) Equal-sized pages and page frames make swapping easy.

#### Question 16: Shell Commands
16. Name and briefly explain three essential shell commands in the XV6 operating system.
Ans:
   a) ls :  Lists the files and directories in the current directory
   b) cp : Copies files or directories
   c) echo : Displays a message or variable value

#### Question 17: Process Synchronization
17. Discuss the concept of process synchronization in XV6. Why is it essential, and what mechanisms are used to achieve it?

#### Question 18: Interrupt Handling
18. Explain the role of interrupts in the XV6 operating system. How are interrupts handled, and what is their significance in system operation?

#### Question 19: Virtual Memory
19. What is virtual memory, and how is it implemented in XV6? Discuss the advantages of using virtual memory.
Ans:
    Virtual Memory is way by which secondary memory can be addressed as though it were part of the main memory. It maps memory addresses used by a program, called virtual addresses, into physical 
    addresses in computer memory.
    

#### Question 20: Boot Process
20. Outline the steps involved in the boot process of XV6. What happens from the moment the computer is powered on to when the XV6 kernel is loaded into memory?

## Answers
1.  b. A Unix-like operating system
2.  c
3.  d
4.  b
5.  d
6.  c
7.  a
8.  a
9.  b
10. b
11. c



