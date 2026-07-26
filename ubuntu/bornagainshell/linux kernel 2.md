## linux kernel 

# how are a syscall & isr different?

An ISR (Interrupt Service Routine) and a system call are both mechanisms that switch the CPU from user mode to kernel mode, but they differ fundamentally in who initiates them and when they occur. 



How They Relate

Interestingly, they often work together. When hardware triggers an ISR (e.g., a key press), the ISR runs quickly to store the data in a buffer.  Later, when a userspace program wants that data, it makes a system call (e.g., read()), which then retrieves the data the ISR previously stored.

# what is a unified interface?

The unified interface refers to the standard set of system calls (functions provided by the kernel) that allow programs to interact with all resources in Linux using the exact same commands, regardless of whether the resource is a text file, a hardware device, a network socket, or a system process. 

This interface relies on four primary operations:

open(): Initiates access to a resource and returns a file descriptor (a simple integer ID). 

read(): Retrieves data from the resource associated with the file descriptor. 

write(): Sends data to the resource associated with the file descriptor. 

close(): Terminates access and releases the resource.

By abstracting complex hardware and kernel internals into this simple file descriptor model, Linux allows developers to write code that works universally.  For example, the same read() command used to open a text document can also read data from a keyboard, a network connection, or the /proc virtual filesystem (which displays real-time system information), without needing specialized drivers or protocols for each specific case. 
