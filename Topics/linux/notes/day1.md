# 🖥️ Operating System & Linux – Complete Notes 📘

---

## 📌 1. What is an Operating System (OS)?

An **Operating System (OS)** is system software that acts as an interface between **users 👤, applications 📱, and hardware 💻**.

### ✅ Main Functions:
- 🧠 Process Management  
- 💾 Memory Management  
- 📁 File Management  
- 🔌 Device Management  
- 🔐 Security & Protection  

---

## 🏷️ 2. Types of Operating Systems

### 🧑‍💻 2.1 Client Operating System

Used by **end users** for daily tasks.

### 📍 Examples:
- 🪟 Windows 10 / 11  
- 🍎 macOS  
- 🐧 Ubuntu Desktop  

### 📌 Uses:
- 🌐 Internet Browsing  
- 💻 Programming  
- 🎮 Gaming  
- 📄 Office Work  

---

### 🖧 2.2 Server Operating System

Used to manage **servers and networks**.

### 📍 Examples:
- 🐧 Linux (Ubuntu Server, RHEL)  
- 🪟 Windows Server  
- 💠 UNIX  

### 📌 Uses:
- 🌍 Web Hosting  
- 🗄️ Database Server  
- ☁️ Cloud Computing  
- 🏢 Enterprise Systems  

---

## ⭐ 3. Why Industry Uses Linux?

Linux is the backbone of **modern IT infrastructure 🚀**.

### 💡 Reasons:
- 🆓 Open Source (Free)  
- 🔐 High Security  
- 💪 Stable & Reliable  
- 📈 Scalable  
- ⚙️ Customizable  
- 🌍 Community Support  

### 🏭 Industry Usage:
- Google, AWS, Azure  
- 📱 Android OS  
- 🏦 Banking Systems  
- 🖥️ Supercomputers  
- 🔄 DevOps  

---

## 🐧 4. Linux Flavours (Distributions)

A **Linux Distribution** = Kernel + Software + Package Manager

### 📦 Popular Distros:

| Distribution | Usage |
|-------------|-------|
| Ubuntu | Beginners, Servers |
| Debian | Stability |
| RHEL | Enterprise |
| CentOS | Server |
| Arch | Advanced |
| Kali | Cyber Security |

---

## 💠 5. What is UNIX?

**UNIX** is an older proprietary OS.

### 🔍 UNIX vs Linux

| UNIX | Linux |
|------|-------|
| Paid 💰 | Free 🆓 |
| Closed 🔒 | Open 🔓 |
| Vendor-based | Community-based |

### 📍 UNIX Examples:
- AIX  
- Solaris  
- HP-UX  

Linux is **UNIX-like**.

---

## 🏗️ 6. Linux Architecture (ASK Model)

### 📐 Layers:

Application 📱
↓
Shell 💬
↓
Kernel 🧠
↓
Hardware 💻



### 📝 Explanation:
- 📱 Application → User software  
- 💬 Shell → Interface  
- 🧠 Kernel → Core OS  
- 💻 Hardware → Physical devices  

---

## 🧠 7. Kernel

The **Kernel** is the heart ❤️ of Linux.

### 🛠️ Functions:
- ⚡ Process Scheduling  
- 💾 Memory Control  
- 📁 File Handling  
- 🔌 Device Drivers  
- 🌐 Network Control  

---

## 💬 8. What is Shell?

Shell is a **command interpreter** that connects **user ➝ kernel**.

It converts commands into system instructions.

---

## 🐚 9. Types of Shell

| Shell | Description |
|-------|-------------|
| sh | Bourne Shell |
| bash | Most used |
| zsh | Advanced |
| fish | User-friendly |
| csh | C Shell |
| ksh | Korn Shell |

Check shell:
```bash
echo $SHELL


📁 10. Linux Files & Directories

✔️ Everything is a file
✔️ Tree structure 🌳
✔️ Starts from / (root)


🌳 11. Root Directory (/) Structure
Folder	Purpose
/	Root
/bin	Commands
/sbin	Admin Commands
/etc	Config Files
/home	User Files
/root	Root User
/var	Logs
/tmp	Temp Files
/usr	Software
/lib	Libraries
/opt	Extra Apps
/boot	Boot Files
/dev	Devices
/proc	Process Info
/sys	Kernel Info
/media	USB/CD
/mnt	Mount Point




📖 12. man Command

man = Manual 📚

Shows documentation of commands.

✍️ Syntax:  man ls

⌨️ Controls:

q → Quit

/ → Search

n → Next


✏️ 13. Vim Editor

Vim is a powerful editor ⚡.

🔁 Modes:

Normal

Insert (i)

Command (:)

📝 Commands:
Command	Work
i	Insert
Esc	Exit
:w	Save
:q	Quit
:wq	Save & Quit
dd	Delete
yy	Copy
p	Paste


🛡️ 15. What is sudo?

sudo = Super User Do 🚀

Allows admin access.

✅ Why sudo?

🔐 Security

🚫 Prevent Damage

📊 Logging

📌 Example:
sudo apt update




👑 16. Root User

Root user = System Admin 👨‍💻

✔️ Full control
❌ Dangerous if misused

Switch:

sudo su



🌐 17. Nginx Web Server

Nginx is a fast web server ⚡.

📌 Uses:

🌍 Website Hosting

🔁 Reverse Proxy

⚖️ Load Balancing

🔗 API Gateway

👍 Advantages:

Fast

Lightweight

Scalable

🛠️ Commands:
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl status nginx

📂 Config File:
/etc/nginx/nginx.conf


<img width="1200" height="800" alt="image" src="https://github.com/user-attachments/assets/9d326a63-ea14-40df-90cd-c37c29e9d321" />



