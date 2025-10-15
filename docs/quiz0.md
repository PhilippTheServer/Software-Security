# Demo instance
Looked at Dockerfile for instructions. Executed commands in this order:

```bash
cp questions_example.json questions.json
docker build -t quiz .
echo 'flag{fake_flag}' > flag
docker run --rm --mount "type=bind,src=$(pwd)/flag,dst=/flag" --cap-add SYS_ADMIN --security-opt apparmor=unconfined -p 1024:1024 -ti quiz
```

Connected to the docker container with:
```bash
nc 127.0.0.1 1024
```

---

## Task summarize

The container showed a couple of questions that needed to be answerd consecutivly. When all the questions where ansered correctly the container spit out the flag.

```bash
Congratulations, here is your flag: flag{fake_flag}
```

---

## Flag

```

```

---

# Real instance

```bash
nc tasks.softsec.rub.de 32787
Welcome to our quiz! You have 120 seconds to answer all questions!
Reverse Engineering (RE) is the process of analyzing a system to:
 (1) hide its components and their interrelationships in complex operations, and make it difficult to create the representations of it in another form or at a higher level.
 (2) identify its components and their interrelationships, and create representations of it in another form or at a higher level.
 (3) extract its components and their interrelationships, and create representations of it in another form or at a lower level.
 (4) identify its components and their interrelationships, and create representations of and execute it as a level code.
> 2

What is the Linux utility that helps track down which syscalls were invoked by a program?
 (1) sysctl
 (2) strings
 (3) strace
 (4) ltrace
> 3

What is the name of the well-known debugger from the GNU project?
 (1) lldb
 (2) windbg
 (3) gdb
 (4) ida
> 3

Consider `int foo = INT_MAX`. What would be the value of foo if you add 1 to foo?
 (1) -2147483648
 (2) 0
 (3) 2147483647
 (4) undefined
> 1

What idiom represents the same as multiplying a number by 2.
 (1) mov rax, 2
 (2) jmp rax
 (3) shl rax, 1
 (4) xor rax, 2
> 3

How are integer arguments passed to functions in Linux on x86_64?
 (1) all arguments are pushed on the stack
 (2) rcx / rdx / r8 / r9, and the rest on the stack
 (3) rax / rbx / rcx / rdx, and the rest on the stack
 (4) rdi / rsi / rdx / rcx / r8 / r9, and the rest on the stack
> 4

When you find a bug lying around in a big company that your government runs. What would be the ethical response to this?
 (1) Try to find a contact for responsible disclosure
 (2) Give to your university professor for free (<3)
 (3) Blackmail the manufacturer
 (4) Sell online
> 1

Which of these is the architecture that considers code as being the same as data
 (1) Turing architecture
 (2) Le Corbusier architecture
 (3) von Neumann architecture
 (4) Harvard architecture
> 3

How is the number 1337 stored in memory (as a 32-bit value)?
 (1) 39050000
 (2) 00001337
 (3) 37130000
 (4) 00000539
> 1

What is the mechanisms name that ensures the stack does not contain code?
 (1) ASLR
 (2) mprotect
 (3) Stack canary
 (4) NX
> 4

How are arguments passed to system calls in Linux on x86_64?
 (1) rdi / rsi / rdx / r10 / r8 / r9
 (2) rax / rbx / rcx / rdx
 (3) rcx / rdx / r8 / r9, and the rest on the stack
 (4) rdi / rsi / rdx / rcx / r8 / r9
> 1

Which syscall do you use for executing programs
 (1) kexec_file_load
 (2) execve
 (3) execl
 (4) sysinfo
> 2

Congratulations, here is your flag: softsec{p1m8aNRm_vXbvausA_QMfle2sWPiduY2pvoknVaTXTRJQsU7SCnqcrln1E9qkdGd}
```

Nothing really todo. Try the questions, look up the correct answer and type it in. The container then gave out the flag.