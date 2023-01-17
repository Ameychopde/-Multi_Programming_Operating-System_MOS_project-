# Os_Simulation_
This project is based on creating Multi-Programming Operating System (MOS) 

# So , What is a Multi-Programming Operating System (MOS) ?
A Multi-Programming Operating System (MOS) is an operating system that allows multiple programs to run concurrently on a computer. This is achieved by allowing each program to run for a short time, called a time slice, and then switching to the next program. This approach allows the computer to efficiently use its resources, such as memory and CPU time, and can improve the overall performance and responsiveness of the system. Some examples of MOS include Windows and Linux. The project on MOS is typically focused on the design and implementation of such an operating system, including the development of the scheduler, memory management, and other system-level components.

Before Starting we shode know some assumption : 
> Jobs may have program errors
> PI interrupt for program errors introduced
> No physical separation between jobs
> Job outputs separated in output file by 2 blank lines
> Paging introduced, page table stored in real memory
> Program pages allocated one of 30 memory block using random number generator
> Load and run one program at a time
> Time limit, line limit, out-of-data errors introduced
> TI interrupt for time-out error introduced
> 2-line messages printed at termination


And here are some notation that we use in the code :

M: memory
IR: Instruction Register (4 bytes)
IR [1, 2]: Bytes 1, 2 of IR/Operation Code
IR [3, 4]: Bytes 3, 4 of IR/Operand Address
M[&]: Content of memory location &
IC: Instruction Counter Register (2 bytes)
R: General Purpose Register (4 bytes)
C: Toggle (1 byte)
PTR: Page Table Register (4 bytes)
PCB: Process Control Block (data structure)
VA: Virtual Address
RA: Real Address
TTC: Total Time Counter
LLC: Line Limit Counter
TTL: Total Time Limit
TLL: Total Line Limit
EM: Error Message
<-- : Loaded/stored/placed into


This are some interrupt values :
SI = 1 on GD
   = 2 on PD
   = 3 on H
TI = 2 on Time Limit Exceeded
PI = 1 Operation Error
   = 2 Operand Error
   = 3 Page Fault


The error message coding use here is as follow :
![Screenshot 2023-01-17 182330](https://user-images.githubusercontent.com/89635899/212904038-9920c1bd-d426-4aac-b2ee-4a3745358cd0.png)



