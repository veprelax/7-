Виконала самостійно Слобожан Софія РПЗ-23А
Лабораторна робота №7 
### Topic: “Creating Script Files and Determining System Hardware Configuration”

#### Objective:
To gain practical skills in working with the Bash command shell. To familiarize with basic actions when working with script files.

#### Material Resources for Classes:
1. **IBM PC Type Computer**: Used for performing all practical tasks.
2. **Windows Operating System and Virtual Machine VirtualBox (Oracle)**: For working with the virtual environment and accessing resources.
3. **GNU/Linux OS (any distribution)**: The main platform for executing scripts and commands.
4. **Cisco Networking Academy Website (netacad.com)**: A resource for accessing online Linux courses that assist in learning and gaining additional knowledge.
---

### Glossary of Terms

1. **Script**: A file containing a series of commands that are executed by a command-line interpreter.
2. **Bash**: A Unix shell and command language that is widely used for scripting.
3. **Command**: An instruction given to a computer program to perform a specific task.
4. **Parameter**: A value that is passed to a command or script to modify its behavior.
5. **Execution**: The process of running a script or command.
6. **Editing**: The act of modifying the contents of a script file.
7. **Mounting**: The process of making a file system accessible at a certain point in the directory tree.
8. **MBR (Master Boot Record)**: A type of partitioning scheme used for hard drives that contains information about the partitions.
9. **GPT (GUID Partition Table)**: A modern partitioning scheme that supports larger disks and more partitions than MBR.

---

### Answers to Questions

#### 1. Describe the concept of a script in the command shell.
A script in the command shell is a text file that contains a sequence of commands that are executed automatically. Scripts allow for the automation of routine tasks, execution of complex commands, and storage for reuse. Scripts are typically written in scripting languages such as Bash and can include conditional statements, loops, and functions.

#### 2. How are scripts created and edited, and what needs to be done to run a script?
Scripts are created using a text editor (e.g., `nano`, `vim`, or `gedit`). To create a script, you need to:
1. Open a text editor.
2. Write the commands you want to execute.
3. Save the file with a `.sh` extension.
4. Grant the file execution permissions using the command `chmod +x script.sh`.
5. Run the script by calling it in the command line, for example, `./script.sh`.

#### 3. What are the main components of a motherboard that you know?
The main components of a motherboard include:
- **CPU (Central Processing Unit)**: The primary computing element of the system.
- **RAM (Random Access Memory)**: Temporary storage for data being used by the CPU.
- **Chipset**: A set of microchips that manages communication between the CPU, memory, and other components.
- **Expansion Slots**: Ports for connecting additional cards, such as graphics or sound cards.
- **Input/Output Ports**: For connecting peripheral devices such as USB, HDMI, and Ethernet.

#### 4. Briefly describe which devices operate with the concepts of MBR and GPT.
**MBR (Master Boot Record)** is used for hard drives and SSDs that have limitations on the number of partitions (up to 4 primary) and maximum size (up to 2 TB). **GPT (GUID Partition Table)** is used for newer hard drives and SSDs that exceed these limitations, allowing for the creation of more partitions (up to 128) and supporting disks larger than 2 TB.

#### 5. What is the essence of the mounting operation, and why is it needed?
The mounting operation is the process by which the operating system makes a file system accessible for use. This is necessary so that users can access data on external storage devices (such as USB drives and hard disks) or virtual file systems. Mounting allows the system to integrate different file systems into a single directory hierarchy.
#### 2.
![image](https://github.com/user-attachments/assets/2735f194-f0ca-4789-92c3-f69967a1cfea)
#### 1. Script for Greeting the Current User
![image](https://github.com/user-attachments/assets/01bcbae2-3b85-4df7-8a16-759b9b00e7f4)
![image](https://github.com/user-attachments/assets/3f05bbd0-302a-4435-aab4-e2f093f65736)
#### 2. Script for Displaying Hardware Configuration Information
![image](https://github.com/user-attachments/assets/6ce0bb21-d99b-4b35-a7d6-995a0acd74ac)
![image](https://github.com/user-attachments/assets/db3cbc98-d00e-4cea-b328-3e930b923f6d)
![image](https://github.com/user-attachments/assets/da7bd758-f36a-4171-ac1c-61fcfa08eec7)
Here are the answers to the control questions:

### 1. What is the difference between the `arch` and `lscpu` commands?
- **`arch`**: This command outputs information about the architecture of the processor on which the system is running, usually indicating the type of architecture (e.g., `x86_64` for 64-bit systems).
- **`lscpu`**: This command provides more detailed information about the processor, including the number of cores, threads, frequency, manufacturer, model, and other characteristics. It is more informative than `arch`.

### 2. Which command can be used to get information about the current system's RAM usage?
To get information about the current system's RAM usage, you can use the command:
```bash
free -h
```
This command outputs information about total memory, used memory, free memory, and cached memory in a human-readable format.

### 3. How can variables be processed in scripts and how can branching and looping scenarios be created?
- **Variable processing**: In Bash scripts, variables can be created by assigning values to them, for example:
  ```bash
  MY_VAR="Hello, World!"
  echo $MY_VAR
  ```
- **Branching**: To create conditional statements, you can use the `if`, `else`, `elif` construct:
  ```bash
  if [ "$MY_VAR" == "Hello, World!" ]; then
      echo "Greeting detected."
  else
      echo "No greeting."
  fi
  ```
- **Loops**: To create loops, you can use `for`, `while`, or `until`:
  ```bash
  for i in {1..5}; do
      echo "Iteration $i"
  done
  ```

### 4. What commands can be used to view the status of connected peripheral devices in the terminal?
- **`lsusb`**: Outputs a list of USB devices connected to the system.
- **`lspci`**: Outputs a list of PCI devices connected to the system.
- **`dmesg`**: Outputs kernel messages that may contain information about the connection and detection of peripheral devices.
- **`fdisk -l`**: Outputs information about all disks and their partitions.

### 5. What are the capabilities of the `gparted` application?
`gparted` (GNOME Partition Editor) is a graphical tool for managing disk partitions. Its capabilities include:
- Creating, deleting, resizing, moving, and formatting partitions.
- Viewing information about partitions, such as file systems, sizes, and mount points.
- Changing the type of file system (e.g., from NTFS to ext4).
- Recovering lost partitions (to a limited extent).
- Supporting various file systems, such as ext2, ext3, ext4, FAT32, NTFS, HFS+, and others.

These capabilities make `gparted` a powerful tool for managing disks and partitions in Linux systems.

### Conclusion
In summary, understanding the differences between commands like `arch` and `lscpu`, as well as how to manage RAM usage, process variables in scripts, and utilize tools like `gparted`, is essential for effective system administration and management in Linux environments.







