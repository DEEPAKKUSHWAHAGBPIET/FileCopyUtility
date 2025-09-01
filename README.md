# File Copy Utility (Low-Level Syscalls)

## 📌 Overview
This project implements a simple **file copy utility in C** using only low-level system calls (`open`, `read`, `write`, `lseek`).  

It also provides a **byte-by-byte comparison tool** to verify the accuracy of the copied file (using built-in commands like `diff` on Linux/macOS or `fc` on Windows).  

The goal is to understand how file I/O works at the **system call level**, without relying on higher-level C library functions like `fopen`, `fread`, or `fwrite`.

---

## ⚙️ Features
- Copy a source file to a destination file using:
  - `open()` – open files
  - `read()` – read file contents
  - `write()` – write data into the destination
  - `lseek()` – (optional) manipulate file offsets if needed
- Compare two files **byte by byte** to ensure correctness.
- Cross-platform:
  - Linux, macOS
  - Windows (via MinGW or WSL)

---

## 🛠️ Compilation
```bash
gcc fileCopyUtility.c -o fileCopyUtility.exe
##▶️ Run
fileCopyUtility.exe <src_file> <destination_file>
##🔍 Verify Byte Accuracy

##On Windows:
fc src.txt des.txt

##On Linux/macOS:
diff src.txt des.txt

