# xv6
xv6 is a re-implementation of Dennis Ritchie's and Ken Thompson's Unix
Version 6 (v6).  xv6 loosely follows the structure and style of v6,
but is implemented for a modern x86-based multiprocessor using ANSI C.

# Priority Scheduling
Priority scheduling involves priority assignment to every process, and processes with higher priorities are carried out first, whereas tasks with equal priorities are carried out on a first-come-first-served (FCFS) or round robin basis.

# In this assignment, I have implemented a Priority Scheduling Algorithm. I have modified following files:

** syscall.h
** defs.h
** user.h
** sysproc.c
** usys.S
** syscall.c
** proc.c
** trap.c
** Makefile

* And added fwe new files:

** ps.c
** nice.c
** time.c
** foo.c

* I added new sys calls like :

** cps
** set_priority
** waitx 

# Report

* On executing the priority based scheduler I found out that the average waiting time was less as compared to the originally implemented  round-robin  algorithm.

** Priority Based Scheduler :
	Average Waiting Time = (443+193+925+1013)/4 = 643.5

** Round Robin Scheduler : 
	Average Waiting Time = (620+2+1036+978)/4 = 659

* I have implemented function set_priority using nice.c. I run the program using 
				nice [pid of the process] [New priority]

this sets the priority of a particular process. 

* I made a program named foo.c . It uses fork() to create some process and then I run a 'for' loop for holding some time of CPU. Between this time I changes priority of a particular process(RUNNABLE) as required.
