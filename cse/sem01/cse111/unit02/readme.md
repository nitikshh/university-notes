## **Unit 2 – Operating System**

# **1. What is an Operating System (OS)?**

An **Operating System (OS)** is **system software** that works as an interface between the **user** and the **computer hardware**.

- Without the OS, a user cannot directly control or use hardware resources like CPU, memory, and I/O devices.

**Main roles of OS:**

1. **Resource Allocator**

   - Assigns CPU time, memory, I/O devices, and files to different processes.
   - Ensures efficient and fair distribution of resources.

2. **Control Program**

   - Controls execution of user programs.
   - Prevents errors and improper use of hardware.

3. **Interface**

   - Provides a medium for users to interact with the computer (CLI, GUI, shells).

---

### Goals of an Operating System

- **Ensure System Stability & Security** → prevent crashes and unauthorized access.
- **Efficient Resource Management** → use CPU, memory, and devices optimally.
- **Enable Multitasking & Multiprogramming** → run multiple tasks at the same time.
- **Provide Abstraction** → simplify hardware details, so users only see high-level functions.
- **User Convenience** → easy interfaces (menus, windows, shells).
- **File Management** → organize data in files/directories for easy access.

---

### **Diagram: Role of an OS**

```
   +----------------------+
   |     User Programs    |
   +----------------------+
              |
              v
   +----------------------+
   |  Operating System    |  <-- Resource Allocator + Control Program
   +----------------------+
   |   CPU | Memory | I/O |
   +----------------------+
              |
              v
         Hardware Layer
```

This diagram shows how the OS acts as a **bridge** between **user programs** and the **hardware**.

---

# **2. System Software vs Application Software**

## **System Software**

- System software is designed to **control, coordinate, and manage the hardware and software resources** of a computer.
- It provides the foundation upon which application software can run.

**Examples:**

- Operating Systems (Windows, Linux, macOS)
- Language translators (Compiler, Interpreter, Assembler)
- Utility programs (antivirus, disk management tools)

**Key Features:**

1. Runs in the **background** to support application software.
2. **General purpose** → not task-specific, but ensures system functions.
3. **Closer to hardware** → directly interacts with CPU, memory, I/O.
4. Required for the **basic functioning** of a computer.

---

## **Application Software**

- Application software is designed to **help users perform specific tasks** or solve particular problems.
- Runs **on top of system software** (it cannot run without it).

**Examples:**

- Microsoft Word, Excel (productivity software)
- VLC Media Player (entertainment)
- Games
- Browsers (Chrome, Firefox)

**Key Features:**

1. **Task-oriented** → designed for specific user needs.
2. Works in the **foreground** (user directly interacts).
3. Depends on **system software** to function.
4. Can be **general-purpose** (Word processors) or **special-purpose** (Hospital management system).

---

### **Diagram: Difference Between System and Application Software**

```
          +-----------------------------------+
          |        Application Software        |
          | (Word, Excel, Games, Browsers etc.)|
          +-----------------------------------+
                          |
                          v
          +-----------------------------------+
          |          System Software           |
          | (OS, Compilers, Assemblers etc.)   |
          +-----------------------------------+
                          |
                          v
                    +-----------+
                    | Hardware  |
                    +-----------+
```

---

# **3. Types of Operating Systems**

An **Operating System (OS)** can be classified into different types based on how it manages resources, users, and tasks.

---

## **1. Batch Operating System**

- **Definition**: Processes jobs in **groups (batches)** without user interaction during execution.
- Jobs are **collected → queued → executed one after another**.
- Efficient for **repetitive and long-running tasks**.

**Examples**: IBM OS/360

✅ **Advantages**

- Automates repetitive tasks
- Good for data processing

❌ **Disadvantages**

- No real-time interaction
- Debugging is difficult

**Diagram: Batch Processing**

```
 Users Submit Jobs
       |
       v
+-----------------+
|   Job Queue     |
+-----------------+
       |
       v
+-----------------+
| Batch Processor |
+-----------------+
       |
       v
   [ Output ]
```

---

## **2. Time-Sharing Operating System**

- Allows **multiple users** to share the system **simultaneously**.
- CPU switches rapidly between users (time slices), creating the **illusion of parallelism**.
- Provides **fast response** and **interactivity**.

**Examples**: UNIX, Multics

✅ **Advantages**

- Supports multitasking
- Efficient CPU utilization

❌ **Disadvantages**

- Complex to manage
- Security issues with multiple users

**Diagram: Time-Sharing**

```
+-----------------------------------+
|          CPU Scheduler            |
+-----------------------------------+
     |      |       |       |
     v      v       v       v
 [User1] [User2] [User3] [User4]
 (Time Slice -> Round Robin)
```

---

## **3. Distributed Operating System**

- Controls **multiple computers** as if they were a **single system**.
- Shares resources across **networked machines**.
- Provides **load balancing** and improves **reliability**.

**Examples**: Amoeba, Locus

✅ **Advantages**

- Resource sharing across systems
- High performance & fault tolerance

❌ **Disadvantages**

- Complex design
- Expensive setup

**Diagram: Distributed OS**

```
+-----------+     +-----------+     +-----------+
|  System A |<--->|  System B |<--->|  System C |
+-----------+     +-----------+     +-----------+
       \             |               /
        \            |              /
         \-----------|-------------/
                 Shared Resources
```

---

## **4. Real-Time Operating System (RTOS)**

- Responds **immediately** to input or events.
- Used where **timing is critical** (robots, aircraft, medical systems).

### Types of RTOS

1. **Hard RTOS** → Strict deadlines (e.g., Airbag system).
2. **Soft RTOS** → Flexible deadlines (e.g., Video streaming).

**Examples**: VxWorks, QNX, RTLinux

✅ **Advantages**

- Predictable and reliable
- Used in safety systems

❌ **Disadvantages**

- Limited multitasking support
- Specialized and costly

**Diagram: RTOS**

```
+-------------------------+
|  Real-Time Scheduler    |
+-------------------------+
   |       |        |
   v       v        v
[Task A] [Task B] [Task C]
 (Must meet strict deadlines)
```

---

## **5. Network Operating System (NOS)**

- Manages **network resources** (printers, files, applications).
- Provides **authentication & security**.
- Uses a **central server** with client machines.

**Examples**: Windows Server, UNIX-based NOS

✅ **Advantages**

- Centralized control
- Resource sharing

❌ **Disadvantages**

- Dedicated server needed
- Costly maintenance

**Diagram: Network OS**

```
           +-----------------+
           |  Central Server |
           +-----------------+
            /   |     |    \
           /    |     |     \
      Client1 Client2 Client3 Client4
```

---

## **6. Mobile Operating System**

- Optimized for **smartphones & tablets**.
- Focuses on **battery efficiency, touch, and apps**.
- Lightweight but powerful.

**Examples**: Android, iOS, HarmonyOS

✅ **Advantages**

- Portable & user-friendly
- Connectivity features (Wi-Fi, 5G, Bluetooth)

❌ **Disadvantages**

- Limited hardware
- Frequent updates required

**Diagram: Mobile OS**

```
+---------------------------------------+
|           Mobile OS Kernel            |
+---------------------------------------+
  |     |       |      |       |     |
  v     v       v      v       v     v
 Apps Sensors Camera Network Touch Battery
```

---

### **Overall Diagram: Types of Operating Systems**

```
   +----------------------------------+
   |          Types of OS             |
   +----------------------------------+
      |     |     |      |     |    |
      v     v     v      v     v    v
   Batch  Time   Dist  RTOS   Net  Mobile
```

---

# **4. Functions of Operating System**

The **Operating System (OS)** is responsible for managing all resources of a computer and providing services to users and applications.
Its main functions include **process, memory, file, storage, I/O, network, security management, and command interpretation**.

---

## **1. Process Management**

- **Definition**: Manages the **creation, scheduling, and termination** of processes.
- Ensures **fair CPU time allocation**.
- Handles **synchronization** and **communication** between processes.
- Uses a **Process Control Block (PCB)** to track process details.

**Process Life Cycle**:
New → Ready → Running → Waiting → Terminated

✅ Ensures efficient **multitasking**.

❌ Poor scheduling may cause **starvation**.

**Diagram: Process Management**

```
        +------+
        | New  |
        +------+
           |
           v
        +-------+
        | Ready |
        +-------+
           |
           v
        +--------+
        | Running|
        +--------+
         /    \
        v      v
   [Waiting] [Terminated]
```

---

## **2. File Management**

- A **file** = collection of data (text, images, code).
- OS manages **creation, deletion, reading, writing, and backup** of files.
- Maintains **directory hierarchy** for organization.

✅ Makes data access easy and organized.

❌ Corruption may cause **data loss**.

**Diagram: File Management**

```
 Root Directory
      |
  +---+---+
  |       |
 UserA   UserB
  |        |
Files   Subdirectories
```

---

## **3. Network Management**

- Manages **connected devices** in a network.
- Ensures **fault handling, performance monitoring, and secure communication**.
- Supports **LAN, WAN, wired, and wireless networks**.

✅ Provides **resource sharing** and reliability.

❌ Vulnerable to **cyberattacks**.

**Diagram: Network Management**

```
 [Device1] ---\
 [Device2] ---->  [Network OS] ----> [Device3]
 [Device4] ---/
```

---

## **4. Main Memory Management**

- Manages **RAM (primary memory)**.
- Tracks which parts are **allocated/free**.
- Allocates memory to processes and **deallocates after completion**.
- Handles **address mapping** during program execution.

✅ Improves RAM efficiency.

❌ Poor allocation → fragmentation.

**Diagram: Memory Management**

```
+-------------------------------------+
| OS | Process A | Free | Process B   |
+-------------------------------------+
```

---

## **5. Secondary Storage Management**

- Manages **hard disks, SSDs, USBs, CDs**.
- Functions include:

  - **Storage allocation**
  - **Free space management**
  - **Disk scheduling**

✅ Stores data permanently.

❌ Slower than main memory.

**Diagram: Secondary Storage**

```
+-----------------------------+
| Disk Blocks Allocation Map  |
+-----------------------------+
| Used | Free | Used | Free   |
+-----------------------------+
```

---

## **6. I/O Device Management**

- Controls **input and output devices** (keyboard, printer, mouse, etc.).
- Provides **device drivers** for hardware communication.
- Uses **buffering and caching** to improve performance.

✅ Ensures smooth hardware–software interaction.

❌ Hardware failure affects OS.

**Diagram: I/O Management**

```
[User Program]
      |
      v
[ I/O Manager ] ---> [ Device Driver ] ---> [ Hardware Device ]
```

---

## **7. Security Management**

- Prevents **unauthorized access** to files, memory, and CPU.
- Protects data integrity and privacy.
- Provides **user authentication, access control, and error detection**.

✅ Keeps system safe.

❌ Misconfigurations may allow **breaches**.

**Diagram: Security Management**

```
[ User Login ]
      |
   [ Authentication ]
      |
   Access Granted → [ Resources ]
   Access Denied  → [ Blocked ]
```

---

## **8. Command Interpreter (Shell)**

- Acts as the **interface between user and OS**.
- Accepts user commands and passes them to the OS for execution.
- Examples: **Windows CMD, UNIX Shell, PowerShell**.

✅ Provides user control.

❌ Wrong commands may cause errors.

**Diagram: Command Interpreter**

```
[User Command] ---> [ Shell / CLI ] ---> [ OS Kernel ] ---> [ Execution ]
```

---

### **Summary Diagram: Functions of OS**

```
     +--------------------------------------------+
     |               Operating System             |
     +--------------------------------------------+
       /    |     |       |      |       |      \
Process   File  Memory  Storage  I/O  Security  Shell
```

---

# **5. Directory Structure**

A **directory** is like a container that holds information about **files and subdirectories**.

- It stores **file names, locations, sizes, and attributes**, but not the actual content.
- Helps in **organizing and accessing files efficiently**.

**Operations on Directories:**

- Create a file / directory
- Delete a file / directory
- Search for a file
- Rename a file
- Traverse the file system
- List directory contents

---

## **1. Single-Level Directory**

- All files are stored in **one directory only**.
- Simple to **implement and understand**.
- **Limitation**: Name conflicts occur when many files exist.

✅ Easy to manage for small systems
❌ Naming conflicts, poor organization

**Diagram: Single-Level Directory**

```
   Root Directory
   +-----------------------------------+
   | file1 | file2 | file3 | file4 ... |
   +-----------------------------------+
```

---

## **2. Two-Level Directory**

- Each user has their own **User File Directory (UFD)**.
- All UFDs are linked to a **Master File Directory (MFD)**.
- Solves the **naming conflict problem**.

✅ Supports multiple users
❌ Still limited flexibility in organization

**Diagram: Two-Level Directory**

```
   Master File Directory (MFD)
   +---------------------------+
   | UserA | UserB | UserC ... |
   +---------------------------+
       |        |
       v        v
   [ UFD-A ]  [ UFD-B ]
   file1...   fileX...
```

---

## **3. Tree-Structured Directory**

- Organizes directories in a **hierarchical structure**.
- Allows **subdirectories** inside directories.
- Has a **root directory** at the top.

✅ Easy to manage and scalable
❌ Traversing may become slow if too deep

**Diagram: Tree-Structured Directory**

```
         Root
          |
    +-----+-----+
    |           |
  UserA       UserB
    |          /   \
 file1   subdir1  subdir2
            |
          fileX
```

---

## **4. Acyclic-Graph Directory**

- Allows **shared directories or files** between users.
- One file may appear in multiple locations.
- Prevents **duplication of files**.

✅ Saves storage by sharing
❌ Managing updates and deletions is complex

**Diagram: Acyclic-Graph Directory**

```
      Root
       |
  +----+----+
  |         |
UserA     UserB
  |         |
 fileX <----+
 (Shared File)
```

---

## **5. General Graph Directory**

- Extension of acyclic-graph but allows **links that form cycles**.
- Provides maximum flexibility.
- But can cause **circular dependencies** (hard to manage).

✅ Very flexible
❌ Risk of cycles, requires careful tracking

**Diagram: General Graph Directory**

```
   Root
    |
  UserA
    |
  fileX
    ↑
    | (Link back creates cycle)
  UserB
```

---

### **Summary: Directory Structures**

| **Type**        | **Description**                         | **Pros**                        | **Cons**                    |
| --------------- | --------------------------------------- | ------------------------------- | --------------------------- |
| Single-Level    | One directory for all files             | Simple, easy to use             | Name conflicts, poor org    |
| Two-Level       | Separate directory for each user        | Solves naming conflicts         | Limited flexibility         |
| Tree-Structured | Hierarchical with subdirectories        | Scalable, organized             | Slow if too deep            |
| Acyclic-Graph   | Shared files/directories without cycles | Saves storage, supports sharing | Complex update management   |
| General Graph   | Links with cycles allowed               | Very flexible                   | Risk of circular dependency |

---

# **6. Bootloader**

A **Bootloader** is a **small program** that loads the **Operating System (OS) kernel** into memory when the computer is powered on.
It is the **first software** that runs after the system’s BIOS/firmware.

---

## **Steps of Booting Process**

1. **Power On Self-Test (POST)**

   - BIOS/UEFI runs basic hardware checks.

2. **BIOS/UEFI Execution**

   - Looks for a **bootable device** (HDD, SSD, USB, etc.).

3. **Master Boot Record (MBR)**

   - Control passes to **MBR**, located at the first sector of the boot disk.

4. **Bootloader Program**

   - Bootloader loads and initializes the **OS kernel**.

5. **OS Kernel Execution**

   - Kernel starts device drivers, services, and user interface.

---

**Diagram: Bootloader Working**

```
+--------+     +--------+     +------------+     +------------+     +---------+
|  BIOS  | --> |  MBR   | --> | Bootloader | --> |   Kernel   | --> |  OS UI  |
+--------+     +--------+     +------------+     +------------+     +---------+
```

---

## **Common Bootloaders**

- **LILO (Linux Loader)**

  - Early bootloader for Linux.
  - Loads kernel directly from disk.

- **LOADLIN (Load Linux from DOS)**

  - Used to boot Linux from DOS/Windows environment.

- **GRUB (GRand Unified Bootloader)**

  - Most widely used Linux bootloader.
  - Supports **multiple operating systems**.

---

## **Bootloader Features**

✅ Allows **multi-boot systems** (choose OS at startup).
✅ Can pass **parameters** to the OS kernel.
✅ Provides a **backup option** if one OS fails.

❌ Misconfigured bootloader may cause **boot failure**.
❌ Complex for beginners to repair.

---

**Diagram: Multi-Boot Loader**

```
+-------------------------------+
|        Bootloader Menu        |
+-------------------------------+
   |              |           |
   v              v           v
[ Windows ]  [ Linux ]   [ MacOS ]
```

---

# **Summary**

- The **bootloader bridges the gap** between hardware initialization (BIOS/UEFI) and the operating system kernel.
- Common bootloaders: **LILO, LOADLIN, GRUB**.
- Essential for **system startup** and **multi-OS environments**.

---

# **7. Kernel & Types of Kernels**

The **Kernel** is the **core part of an Operating System**.

- It manages **system resources** (CPU, memory, I/O devices).
- Acts as a **bridge between hardware and software**.
- Loads **first** when the computer starts.

---

## **Functions of Kernel**

- **Process Management** → scheduling, creation, termination.
- **Memory Management** → allocation/deallocation.
- **Device Management** → handling drivers & I/O.
- **File System Management** → controls access to files.
- **Security & Protection** → prevents unauthorized access.

**Diagram: Kernel Role**

```
+----------------------+
|   Application Layer  |
+----------------------+
          |
          v
+---------------------+
|       Kernel        |
|  (Process, Memory,  |
|   I/O, File, Sec.)  |
+---------------------+
          |
          v
+---------------------+
|     Hardware        |
+---------------------+
```

---

## **Types of Kernels**

---

### **1. Monolithic Kernel**

- Entire OS works in **kernel space**.
- All services (file system, device drivers, memory) run as a **single large process**.
- Very **fast performance**, but **hard to debug**.

**Examples**: Linux, UNIX, MS-DOS

**Diagram: Monolithic Kernel**

```
+------------------------------------+
|          Monolithic Kernel         |
|  [ File | Memory | Drivers | FS ]  |
+------------------------------------+
          |
        Hardware
```

✅ High performance
❌ Large, less secure

---

### **2. Microkernel**

- Only **essential services** run in kernel space.
- Other services run in **user space** (drivers, file systems).
- More **stable and secure**, but **slower** due to context switching.

**Examples**: QNX, Minix, early MacOS

**Diagram: Microkernel**

```
+-------------------+    +-------------------+
|    User Space     | -> | Device Drivers    |
| (FS, Drivers, UI) | -> | File Systems      |
+-------------------+    +-------------------+
           |
           v
 +----------------+
 |   Microkernel  |
 | (CPU, Memory,  |
 |   IPC only)    |
 +----------------+
       |
    Hardware
```

✅ Secure & modular
❌ Slower

---

### **3. Hybrid Kernel**

- Combination of **Monolithic + Microkernel**.
- Core services in kernel space, but some are modular.
- Provides **balance between performance and stability**.

**Examples**: Windows NT, modern macOS

**Diagram: Hybrid Kernel**

```
+----------------------------+
|        Hybrid Kernel       |
|    Core (CPU, Memory)      |
|    + Loadable Modules      |
+----------------------------+
            |
         Hardware
```

✅ Balance of speed & security
❌ More complex

---

### **4. Nano Kernel**

- Extremely **small kernel** with very minimal services.
- Often used in **real-time or embedded systems**.

**Examples**: Used in research & embedded devices

**Diagram: Nano Kernel**

```
+-----------------+
|   Nano Kernel   |
| (Minimal tasks) |
+-----------------+
        |
     Hardware
```

✅ Very lightweight
❌ Limited features

---

### **5. Exo Kernel**

- Provides **direct hardware access** to applications.
- Kernel is just a **thin abstraction layer**.
- Applications manage their **own resources**.

**Examples**: MIT Exokernel (experimental)

**Diagram: Exo Kernel**

```
Applications <---- Direct Access ----> Hardware
          \
           \__ Exo Kernel (thin layer)
```

✅ High performance, flexible
❌ Complex for developers

---

### **6. Modular Kernel**

- Based on **Monolithic Kernel** but supports **dynamically loadable modules**.
- Features can be **added/removed at runtime**.
- Used in **modern Linux systems**.

**Examples**: Linux (with kernel modules)

**Diagram: Modular Kernel**

```
+-----------------------------+
| Modular Kernel              |
| [ Core ] + [ Plug-in Mods ] |
+-----------------------------+
              |
           Hardware
```

✅ Easy to maintain & extend
❌ Still larger than microkernel

---

# **Summary Table: Types of Kernels**

| **Kernel Type** | **Features**                     | **Examples**        | **Pros**                   | **Cons**               |
| --------------- | -------------------------------- | ------------------- | -------------------------- | ---------------------- |
| Monolithic      | All OS services in kernel space  | Linux, UNIX, MS-DOS | Fast, efficient            | Hard to maintain/debug |
| Microkernel     | Only essentials in kernel space  | QNX, Minix          | Secure, modular            | Slower performance     |
| Hybrid          | Mix of monolithic & microkernel  | Windows NT, macOS   | Balance of speed & safety  | Complex                |
| Nano            | Very small, minimal services     | Embedded systems    | Lightweight, efficient     | Very limited features  |
| Exo             | Direct hardware access for apps  | MIT Exokernel       | Flexible, high performance | Hard to program/manage |
| Modular         | Monolithic with loadable modules | Modern Linux        | Extensible, maintainable   | Still larger in size   |

---

# **8. Programming Language Levels**

Programming languages can be classified into **different levels** based on how close they are to machine hardware or human understanding.

---

## **1. Machine Language**

- Lowest-level language, directly understood by the **CPU**.
- Written in **binary (0s and 1s)**.
- Very **fast** but **hard to read/write**.
- Machine-dependent → not portable.

**Example:**

```
10110000 01100001
```

**Diagram: Machine Language**

```
[Binary Code] --> [CPU Execution] --> [Output]
```

✅ Very fast execution
❌ Difficult to program, error-prone

---

## **2. Assembly Language**

- Low-level language using **mnemonics** (symbols) instead of binary.
- Provides **one-to-one mapping** with machine instructions.
- Requires an **Assembler** to convert into machine code.
- Still **hardware-dependent**.

**Examples:**

```
MOV A, 5
ADD A, B
```

**Diagram: Assembly Language**

```
[Assembly Code] --(Assembler)--> [Machine Code] --> [CPU]
```

✅ Easier than binary
❌ Still complex and machine-specific

---

## **3. High-Level Language (HLL)**

- Closer to **human language**, easy to read/write.
- Portable across systems (not hardware-dependent).
- Requires a **compiler or interpreter** to run.
- Supports complex operations, data structures, and libraries.

**Examples:** C, C++, Java, Python, JavaScript

**Diagram: High-Level Language**

```
[High-Level Code] --(Compiler/Interpreter)--> [Machine Code] --> [CPU]
```

✅ Easy to learn and debug
❌ Slower than low-level due to translation overhead

---

# **Comparison of Language Levels**

| **Language Level**  | **Representation**   | **Translator**   | **Pros**                       | **Cons**                       |
| ------------------- | -------------------- | ---------------- | ------------------------------ | ------------------------------ |
| Machine Language    | Binary (0s & 1s)     | None             | Fast execution, direct control | Very hard to code, error-prone |
| Assembly Language   | Mnemonics (ADD, MOV) | Assembler        | Easier than binary, efficient  | Still hardware dependent       |
| High-Level Language | English-like syntax  | Compiler/Interp. | Portable, easy to learn/debug  | Slower, requires translation   |

---

### **Summary Diagram: Language Levels**

```
High-Level Language  --->  Assembly Language  --->  Machine Language
   (C, Python)               (MOV, ADD)              (01010101)
```

---

# **9. Steps in Program Development**

Developing a program is not just about writing code. It is a **step-by-step process** to ensure the program works correctly, is easy to maintain, and solves the intended problem.

---

## **Step 1: Problem Definition**

- Clearly understand **what the program should do**.
- Identify the **inputs, expected outputs, and constraints**.
- Define the **purpose** of the program.

✅ A well-defined problem avoids confusion later.

**Example**:

- Problem: Calculate the average marks of 5 subjects.
- Input: Marks in 5 subjects.
- Output: Average of marks.

**Diagram: Problem Definition**

```
  Problem Statement
        ↓
   Identify Inputs → Processing → Output
```

---

## **Step 2: Planning the Solution**

- Decide **how to solve the problem** logically.
- Use tools like:

  - **Algorithms** (step-by-step instructions)
  - **Flowcharts** (visual representation)
  - **Pseudocode** (English-like code)

✅ Planning saves time and reduces errors.

**Diagram: Flowchart Example (Find Average)**

```
   +-------------------+
   |     Start         |
   +-------------------+
           |
           v
   +-------------------+
   |   Input 5 marks   |
   +-------------------+
           |
           v
   +-------------------+
   | Sum = m1+m2+...m5 |
   +-------------------+
           |
           v
   +-------------------+
   |   Avg = Sum/5     |
   +-------------------+
           |
           v
   +-------------------+
   |   Print Average   |
   +-------------------+
           |
           v
   +-------------------+
   |      End          |
   +-------------------+
```

---

## **Step 3: Writing the Code**

- Convert the **planned solution** into a **programming language** (C, Python, Java, etc.).
- Follow proper **syntax and structure**.
- Add **comments** for readability.

✅ This is the translation of logic into real code.

---

## **Step 4: Compiling & Debugging**

- **Compile** → Converts source code into machine code.
- **Debug** → Remove errors in the program.

  - **Syntax Errors**: Mistakes in language rules.
  - **Logical Errors**: Wrong logic, wrong results.
  - **Runtime Errors**: Errors during execution (e.g., divide by zero).

✅ Debugging ensures the program runs correctly.

**Diagram: Error Checking Cycle**

```
Write Code → Compile → Errors Found?
       |                 |
      No                Yes
       |                 |
     Run Program    Fix & Debug
```

---

## **Step 5: Testing the Program**

- Run the program with **sample inputs**.
- Compare outputs with **expected results**.
- Test for:

  - **Correctness**
  - **Efficiency**
  - **Boundary conditions** (e.g., input = 0).

✅ Ensures the program works in all cases.

---

## **Step 6: Deployment & Maintenance**

- **Deploy**: Install and run the program in the **real environment**.
- **Maintain**: Fix bugs, update for new requirements, optimize performance.

✅ Maintenance is the **longest phase** in software life.

**Diagram: Full Program Development Life Cycle**

```
Problem → Plan → Code → Compile/Debug → Test → Deploy/Maintain
```

---

### **✨ Summary**

| **Step**               | **Purpose**                                 |
| ---------------------- | ------------------------------------------- |
| **Problem Definition** | Understand what needs to be solved          |
| **Plan Solution**      | Design using algorithm/flowchart/pseudocode |
| **Write Code**         | Implement in a programming language         |
| **Compile & Debug**    | Remove syntax, logical, runtime errors      |
| **Test Program**       | Check output with sample inputs             |
| **Deploy & Maintain**  | Real-world use, fix bugs, make updates      |

---

# **10. Compilation vs Execution**

A program written in a **high-level language** (C, C++, Java, Python, etc.) cannot be directly understood by the computer.
It must go through two main phases: **Compilation** and **Execution**.

---

## **1. Compilation**

- **Definition**: The process of converting **source code (human-readable)** into **machine code (binary)** using a **compiler**.
- Produces an **object file/executable file**.

### **Key Points**

- **Checks syntax errors** (missing semicolon, wrong keywords, etc.).
- **Optimizes** the code for performance.
- Once compiled successfully, the program can be **executed multiple times** without recompilation.

✅ **Faster execution** (code is pre-translated).
❌ **Takes extra time initially** for compilation.

**Diagram: Compilation Process**

```
  [ Source Code (.c/.cpp/.java) ]
                |
          ( Compiler )
                v
[ Object Code / Executable File (.exe) ]
```

---

## **2. Execution**

- **Definition**: The process of **running the compiled program** on the computer.
- The **CPU executes instructions** line by line from the executable file.

### **Key Points**

- The program **performs tasks** as designed (calculations, file handling, I/O, etc.).
- May still produce **runtime errors** (divide by zero, invalid input).
- After execution, system resources (CPU, memory) are released.

✅ **Direct output** for the user.
❌ Errors during execution may cause program crashes.

**Diagram: Execution Process**

```
    [ Executable File (.exe) ]
                |
         ( Loaded into RAM )
                v
   [ CPU Executes Instructions ]
                v
          [ Program Output ]
```

---

## **3. Compilation vs Execution – Key Differences**

| **Aspect**     | **Compilation**                           | **Execution**                       |
| -------------- | ----------------------------------------- | ----------------------------------- |
| **Definition** | Translation of source code → machine code | Running the program instructions    |
| **Performer**  | Done by **Compiler**                      | Done by **CPU / Interpreter**       |
| **Errors**     | Detects **syntax & semantic errors**      | Detects **runtime errors**          |
| **Output**     | **Executable file (.exe/.class/.o)**      | Actual **program output (results)** |
| **Frequency**  | Done **once** (per code change)           | Done **every time program runs**    |
| **Speed**      | **Slower** (takes time to compile)        | **Faster** (already compiled code)  |

---

## **4. Overall Flow Diagram**

```
    Source Code (.c/.cpp/.java)
          |
       Compilation
          |
   Executable File (.exe/.class)
          |
       Execution
          |
      Final Output
```

---

✨ **In short:**

- **Compilation** = Prepare the program (translation to machine code).
- **Execution** = Run the program (instructions performed).

---

# **11. Translator Programs**

A computer only understands **machine language (0s and 1s)**.
Programs written in **high-level** or **assembly language** must be translated into machine code.
This is done by **Translator Programs**.

---

## **Types of Translator Programs**

### **1. Compiler**

- **Definition**: Converts the **entire source code** into **machine code** **before execution**.
- Produces an **object file/executable file**.

**Features:**

- Detects **all syntax errors** at once.
- Once compiled, the program runs **very fast**.
- Languages: **C, C++, Java**.

✅ Efficient for large programs.
❌ Compilation takes more time initially.

**Diagram: Compiler Working**

```
[ Source Code ] --(Compiler)--> [ Executable File ] --> Run --> [ Output ]
```

---

### **2. Interpreter**

- **Definition**: Converts **one line of code at a time** into machine code **during execution**.
- Does not create a separate executable file.

**Features:**

- Stops immediately when an error is found.
- Slower than compiler (translation happens each time).
- Languages: **Python, JavaScript, Ruby**.

✅ Easy to debug (line-by-line execution).
❌ Slower for large programs.

**Diagram: Interpreter Working**

```
[ Source Code ]
       |
 (Interpreter – Line by Line)
       v
[ Direct Execution / Output ]
```

---

### **3. Assembler**

- **Definition**: Converts **assembly language** (mnemonics like MOV, ADD, SUB) into **machine code**.
- Acts as a bridge between **low-level programming** and hardware.

**Features:**

- One-to-one mapping between assembly instructions and machine code.
- Used in **embedded systems & OS development**.

✅ Very close to hardware (efficient).
❌ Hardware dependent (not portable).

**Diagram: Assembler Working**

```
[ Assembly Code ] --(Assembler)--> [ Machine Code (0s & 1s) ] --> [ CPU Execution ]
```

---

## **Comparison of Translator Programs**

| **Aspect**         | **Compiler**                       | **Interpreter**                  | **Assembler**                      |
| ------------------ | ---------------------------------- | -------------------------------- | ---------------------------------- |
| **Input**          | High-level language (C, C++, Java) | High-level language (Python, JS) | Assembly language (MOV, ADD, SUB)  |
| **Translation**    | Entire code at once                | Line by line                     | One assembly instruction at a time |
| **Output**         | Executable file                    | Direct execution (no file)       | Machine code                       |
| **Speed**          | Fast execution after compilation   | Slower (translates every run)    | Very fast (close to hardware)      |
| **Error Handling** | Shows all errors after compilation | Stops immediately at error       | Syntax errors in mnemonics         |

---

## **Overall Diagram: Translator Programs**

```
 High-Level Language ----> [ Compiler ] ---> Machine Code
 High-Level Language ----> [ Interpreter ] ---> Direct Execution
 Assembly Language   ----> [ Assembler ] ---> Machine Code
```

---

✨ **In summary:**

- **Compiler** → Whole program → Executable file → Fast execution.
- **Interpreter** → Line-by-line translation → Immediate execution → Easier debugging.
- **Assembler** → Assembly → Machine code → Close to hardware.

---

End Of Unit
```
This is the end
Hold your breath and count to ten
Feel the Earth move and then
Hear my heart burst again
```
