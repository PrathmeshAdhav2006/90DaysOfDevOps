# 🐧 Advanced Linux & Server Administration Notes 📘🚀

==================================================

🔐 SSH (Secure Shell)
--------------------------------------------------

SSH is a secure network protocol used to connect to remote servers securely.

• Encrypted communication 🔒
• Remote login 🖥️
• Secure file transfer 📁
• Authentication using keys/passwords 🔑

Default SSH Port:
22

--------------------------------------------------

🔑 SSH Key Generation (ssh-keygen)
--------------------------------------------------

Used to generate public and private keys.

Command:
ssh-keygen

Keys Created:
• Private Key → id_rsa 🔐
• Public Key → id_rsa.pub 🔓

Public key is stored on server in:
~/.ssh/authorized_keys

--------------------------------------------------

🌐 SSH Connection Process (Local → EC2)
--------------------------------------------------

1. SSH client sends request
2. Server responds
3. Key authentication happens
4. Secure encrypted session starts

Command to connect:
chmod 400 mykey.pem
ssh -i mykey.pem ubuntu@EC2_PUBLIC_IP

--------------------------------------------------

🔁 Connect Two Servers (EC2 ↔ EC2)
--------------------------------------------------

Steps:

1. Generate key on Server1
ssh-keygen

2. Copy public key to Server2
ssh-copy-id user@server2

OR manually paste id_rsa.pub into:
~/.ssh/authorized_keys

3. Connect without password
ssh user@server2

--------------------------------------------------

✍️ Write File Using echo
--------------------------------------------------

Overwrite file:
echo "Hello Linux" > file.txt

Append to file:
echo "New Line" >> file.txt

--------------------------------------------------

📤 SCP (Secure Copy Protocol)
--------------------------------------------------

Used to copy files securely between servers using SSH.

Upload file:
scp file.txt user@ip:/path

Download file:
scp user@ip:/path/file.txt .

--------------------------------------------------

👤 Linux Users
--------------------------------------------------

Linux is a multi-user operating system.

Types of users:
• Root user 👑
• Normal user 👤
• System user ⚙️

--------------------------------------------------

➕ Create User
--------------------------------------------------

sudo useradd user1
sudo passwd user1

Home directory:
/home/user1

--------------------------------------------------

🔐 Default User Permissions (umask)
--------------------------------------------------

Check umask:
umask

Example value:
0022

Result:
Directories → 755
Files → 644

--------------------------------------------------

👥 Groups in Linux
--------------------------------------------------

Why groups?
• Manage permissions easily
• Team access control
• Better security 🔐

Create group:
sudo groupadd devops

Add user to group:
sudo usermod -aG devops user1

OR
sudo gpasswd -a user1 devops

Check groups:
groups user1

--------------------------------------------------

📁 File Permissions
--------------------------------------------------

View permissions:
ls -l

Example:
-rwxr-xr--

Meaning:
Owner → rwx
Group → r-x
Others → r--

--------------------------------------------------

🔢 Permission (Octal) Table
--------------------------------------------------

4 → Read (r)
2 → Write (w)
1 → Execute (x)

7 = rwx
6 = rw-
5 = r-x

--------------------------------------------------

🔧 chmod (Change Mode)
--------------------------------------------------

Numeric method:
chmod 755 file.txt

Symbolic method:
chmod u+x file.txt

--------------------------------------------------

👑 chown (Change Owner)
--------------------------------------------------

Change owner and group:
chown user:group file.txt

Example:
chown user1:devops test.txt

--------------------------------------------------

📜 Logs in Linux
--------------------------------------------------

Logs store system activity and errors 📝

Log locations:
• /var/log/syslog → System logs
• /var/log/auth.log → Authentication logs
• /var/log/messages → General logs
• /var/log/nginx → Nginx logs

--------------------------------------------------

🔍 grep Command
--------------------------------------------------

Search text patterns.

grep "error" file.txt

Useful options:
-i → ignore case
-n → line number
-r → recursive
-v → exclude pattern

--------------------------------------------------

📊 awk Command
--------------------------------------------------

Used for column-based text processing.

Print first column:
awk '{print $1}' file.txt

With condition:
awk '$3 > 100 {print $1}' file.txt

Using if condition:
awk '{if($2>=50) print $1}' marks.txt

--------------------------------------------------

✂️ sed Command
--------------------------------------------------

Replace text:
sed 's/old/new/g' file.txt

Delete line:
sed '2d' file.txt

--------------------------------------------------

🔗 Pipe Operator ( | )
--------------------------------------------------

Pass output of one command to another.

Example:
ps aux | grep root

--------------------------------------------------

🆔 uniq Command
--------------------------------------------------

Remove duplicate lines.

sort file.txt | uniq

Count duplicates:
uniq -c file.txt

--------------------------------------------------

🔎 find Command
--------------------------------------------------

Search files and directories.

find /home -name file.txt
find / -size +100M
find . -type f
find . -mtime -1

--------------------------------------------------

🌐 Networking Commands
--------------------------------------------------

IP information:
ip a
ifconfig

Connectivity test:
ping google.com

Check ports:
netstat -tulnp
ss -tulnp

DNS lookup:
nslookup google.com
dig google.com

Download tools:
curl
wget

--------------------------------------------------

📁 Important User Files
--------------------------------------------------

/etc/passwd → User information
/etc/shadow → Password hashes
/etc/group → Group details

--------------------------------------------------

🛠️ User Information Commands
--------------------------------------------------

whoami
who
id
users

--------------------------------------------------

🧠 SUMMARY
--------------------------------------------------

✔ SSH for secure access  
✔ SCP for file transfer  
✔ Users & Groups for access control  
✔ chmod & chown for permissions  
✔ grep, awk, sed for text processing  
✔ Logs for monitoring  
✔ Networking commands for troubleshooting  

==================================================
🎉 END OF NOTES 🚀

