Description
In Unix and Unix-like computer operating systems, a file descriptor (FD, less frequently fildes) is a unique identifier (handle for a file or other input/output resource, such as a pipe or network socket.

File descriptors typically have non-negative integer values, with negative values being reserved to indicate "no value" or error conditions.

File descriptors are a part of the POSIX API. Each Unix process (except perhaps daemons) should have three standard POSIX file descriptors, corresponding to the three standard streams:

Integer Value	Name	<unistd.h> symbolic constant	<stdio.h> file stream
0	Standard input	STDIN_FILENO	stdin
1	Standard output	STDOUT_FILENO	stdout
2	Standard error	STDERR_FILENO	stderr
Operations on File Descriptors
The following lists typical operations on file descriptors on modern Unix-like systems. Most of these functions are declared in the <unistd.h> header, but some are in the <fcntl.h> header instead.

Creating File Descriptors
open()
creat()
socket()
accept()
socketpair()
pipe()
epoll_create() (Linux)
signalfd() (Linux)
eventfd() (Linux)
timerfd_create() (Linux)
memfd_create() (Linux)
userfaultfd() (Linux)
fanotify_init() (Linux)
inotify_init() (Linux)
clone() (with flag CLONE_PIDFD, Linux)
pidfd_open() (Linux)
open_by_handle_at() (Linux)
Contents/Files
File 0-read_textfile.c is a function that reads a text file and prints it to the POSIX standard output.

File 1-create_file.c is a function that creates a file.

File 100-elf_header.c is a program that displays the information contained in the ELF header at the start of an ELF file.

File 2-append_text_to_file.c is a function that appends text at the end of a file.

File 3-cp.c is a program that copies the content of a file to another file.

File main.h is the header file that contains all these function prototypes.
