# 🐧 Linux Fundamentals — TryHackMe

**Platform:** [TryHackMe](https://tryhackme.com) | **Rooms Completed:** Linux Fundamentals Parts 1, 2 & 3

---

## 📋 Objective

Complete the TryHackMe Linux Fundamentals learning path to build foundational command-line skills used daily in cloud, DevOps, and cybersecurity roles. This includes navigating the Linux file system, managing files and permissions, transferring data over a network, and monitoring system processes — all hands-on inside live virtual machines.

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| **TryHackMe** | Browser-based lab environment with guided VMs |
| **Linux Terminal (Bash)** | All command execution |
| **GNU nano** | Terminal-based text editor |
| **python3 http.server** | Spin up a simple HTTP file server |
| **wget** | Download files over HTTP from a remote host |
| **AttackBox (TryHackMe)** | Remote Linux machine used for networking tasks |

---

## ✅ Skills Learned

- Navigating the Linux file system (`ls`, `cd`, `pwd`, `find`)
- Reading and creating files (`cat`, `touch`, `nano`)
- Moving and organizing files/directories (`mv`, `mkdir`)
- Understanding file types (`file` command)
- Managing file permissions with `ls -lh` and `chmod`
- Switching users with `su` and understanding access control
- Hosting a file over HTTP with `python3 -m http.server`
- Downloading files from a remote machine using `wget`
- Viewing hidden files with `ls -a`
- Monitoring running processes with `ps` and `top`
- Scheduling tasks with `crontab` (cron jobs)

---

## 📸 Step-by-Step Walkthrough

---

### Step 1 — Navigating the File System

Commands practiced: `ls`, `cd`, `cat`, `pwd`, `find`

Explored the home directory, navigated into `folder4`, read `note.txt` using `cat`, confirmed location with `pwd`, then used `find -name note.txt` to locate the file from the home directory.

<img width="1366" height="768" alt="Linux fundamentals (1)" src="https://github.com/user-attachments/assets/53761270-a06b-46ff-a4aa-515ec293ead3" />

---

### Step 2 — Creating & Moving Files

Commands practiced: `touch`, `mv`, `mkdir`, `file`, `cat`

Created a new file with `touch newnote`, identified an unknown file type using the `file` command (returned `ASCII text`), moved `myfile` into `myfolder` with `mv`, then read its contents — revealing a hidden flag.

<img width="1366" height="768" alt="Linux fundamentals (2)" src="https://github.com/user-attachments/assets/083e2b9a-2690-4c6f-9095-480f0f2927bc" />

---

### Step 3 — File Permissions & Switching Users

Commands practiced: `ls -lh`, `su`, `cat`, `chmod`, `pwd`, `cd`

Ran `ls -lh` to view file ownership and permissions. Switched to `user2` with `su user2` and successfully read the `important` file (which contained a flag). Explored `chmod` syntax and navigated back to the home directory.

<img width="1366" height="768" alt="Linux fundamentals (3)" src="https://github.com/user-attachments/assets/c3aead80-a55c-4b23-b6b7-b493a2843a75" />

---

### Step 4 — Text Editing with Nano

Tool used: `nano`

Opened the `nano` text editor and created a new file called `myfile`. Typed content directly into the terminal editor, demonstrating basic file creation and editing without a GUI.

<img width="1366" height="768" alt="Linux fundamentals (4)" src="https://github.com/user-attachments/assets/4a4081c6-5e44-4984-a401-985df2e8c4ca" />

---

### Step 5 — Hosting a File Server with Python

Command practiced: `python3 -m http.server`

Launched a lightweight HTTP server on port 8000 using Python's built-in module. Confirmed a successful `GET` request in the server logs when the remote machine fetched `.flag.txt` — simulating real file transfer between Linux hosts.

<img width="1366" height="768" alt="Linux fundamentals (5)" src="https://github.com/user-attachments/assets/dba91302-f1fd-48c8-b4aa-4f577ff1873c" />

---

### Step 6 — Downloading Files with wget

Command practiced: `wget`

From the remote AttackBox machine, used `wget` to download `.flag.txt` from the HTTP server running on the other VM. Successfully connected, received a `200 OK` response, and saved the file locally.

<img width="1366" height="768" alt="Linux fundamentals (6)" src="https://github.com/user-attachments/assets/2101622f-2b73-4f51-bb11-05c94b804dd6" />

---

### Step 7 — Viewing Hidden Files

Command practiced: `ls -a`, `cat`

Used `ls -a` to reveal hidden dotfiles (files/directories starting with `.`). Spotted `.flag.txt` in the directory listing, then read it with `cat` to retrieve the flag.

<img width="1366" height="768" alt="Linux fundamentals (7)" src="https://github.com/user-attachments/assets/afbaa5f3-68cd-4a23-b840-8fa0999ac827" />

---

### Step 8 — Viewing Running Processes

Command practiced: `ps`

Used the `ps` command to list active processes in the current session. Output showed the running `bash` shell and `ps` itself, demonstrating basic process visibility.

<img width="1366" height="768" alt="Linux fundamentals (8)" src="https://github.com/user-attachments/assets/d6eb240e-5eb7-4336-a814-c68d93ec803d" />

---

### Step 9 — Real-Time Process Monitoring

Command practiced: `top`

Launched `top` for a live, real-time view of system resources — CPU usage, memory, swap, and a ranked list of all running processes with their PIDs, users, and resource consumption.

<img width="1366" height="768" alt="Linux fundamentals (9)" src="https://github.com/user-attachments/assets/cb73cf63-97a2-4e24-9527-3dea8762237a" />

---

### Step 10 — Scheduling Tasks with Crontab

Command practiced: `crontab -e`

Opened the crontab editor using `nano` and reviewed the cron job syntax. Added a `@reboot` entry to run a script (`/var/opt/processes.sh`) automatically on system startup — a common automation pattern in server environments.

<img width="1366" height="768" alt="Linux fundamentals (10)" src="https://github.com/user-attachments/assets/00f3a41e-3f98-471d-a996-2e10fc6ccc55" />

---
