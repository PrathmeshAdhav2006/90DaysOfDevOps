# 🐚 Shell Scripting, Automation & AWS S3 Notes 📘🚀

==================================================

📌 What is Shell Scripting?
--------------------------------------------------

Shell scripting is writing a series of Linux commands in a file to automate tasks.

• Used for automation 🤖
• System administration 🛠️
• Backup & monitoring 📦
• DevOps pipelines 🔄

Script file extension: .sh

Example:
backup.sh

--------------------------------------------------

📍 What is /bin/bash ?
--------------------------------------------------

/bin/bash is the path of Bash shell (Bourne Again Shell).

Used in script header (Shebang):

#!/bin/bash

It tells system:
👉 "Run this script using Bash shell"

--------------------------------------------------

💬 Comments in Shell Script
--------------------------------------------------

Used to explain code.

Single-line comment:
# This is a comment

Example:
# This script takes backup

There is no multi-line comment officially.

--------------------------------------------------

⚙️ Make Script Executable
--------------------------------------------------

Give execute permission:

chmod +x script.sh

Check:
ls -l script.sh

Output should contain:
x (execute)

--------------------------------------------------

▶️ How to Execute Script
--------------------------------------------------

Method 1:
./script.sh

Method 2:
bash script.sh

Method 3:
sh script.sh

--------------------------------------------------

📝 First Shell Script
--------------------------------------------------

#!/bin/bash

echo "Hello Linux"

Save as: hello.sh

Run:
./hello.sh

--------------------------------------------------

📌 Variables in Shell
--------------------------------------------------

Syntax:
name=value

Example:
user=linux

Access:
echo $user

Important Rule:
❌ No space before/after =

Correct:
a=10

Wrong:
a = 10

--------------------------------------------------

📥 User Input (read)
--------------------------------------------------

read command is used to take input.

Example:

#!/bin/bash
echo "Enter name:"
read name
echo "Hello $name"

--------------------------------------------------

🌍 Environment Variables & printenv
--------------------------------------------------

Environment variables are system variables.

Show all:
printenv

Example:
printenv HOME

Common variables:
PATH
HOME
USER
SHELL

--------------------------------------------------

📌 Command Line Arguments
--------------------------------------------------

Arguments passed while running script.

$0 → Script name
$1 → First argument
$2 → Second argument
$@ → All arguments
$# → Count

Example:

./test.sh apple banana

Script:

#!/bin/bash
echo "First: $1"
echo "Second: $2"
echo "Total: $#"

--------------------------------------------------

❓ If-Else Conditions
--------------------------------------------------

Syntax:

if [ condition ]
then
   commands
fi

Example:

#!/bin/bash
if [ $1 -gt 10 ]
then
  echo "Greater than 10"
else
  echo "Less than 10"
fi

Operators:
-eq = equal
-ne = not equal
-gt = greater
-lt = less
-ge = greater equal
-le = less equal

--------------------------------------------------

🔀 Case Statement
--------------------------------------------------

Used for menu programs.

Example:

#!/bin/bash
read ch

case $ch in
1) echo "One" ;;
2) echo "Two" ;;
*) echo "Invalid" ;;
esac

--------------------------------------------------

🔁 Loops
--------------------------------------------------

For Loop:

for i in 1 2 3 4
do
 echo $i
done

While Loop:

i=1
while [ $i -le 5 ]
do
 echo $i
 i=$((i+1))
done

Until Loop:

i=1
until [ $i -gt 5 ]
do
 echo $i
 i=$((i+1))
done

--------------------------------------------------

🧩 Functions
--------------------------------------------------

Used to reuse code.

Syntax:

function myfun() {
 echo "Hello"
}

Call:
myfun

Example:

add() {
 echo $(( $1 + $2 ))
}

add 10 20

--------------------------------------------------

📐 Arithmetic Operations
--------------------------------------------------

Method 1:
expr 5 + 3

Method 2:
$((5+3))

Example:
a=10
b=20
c=$((a+b))
echo $c

--------------------------------------------------

🔗 Mixed Concepts Example
--------------------------------------------------

#!/bin/bash

backup() {
  zip backup.zip *.txt
}

if [ $# -eq 0 ]
then
  echo "No arguments"
else
  backup
  echo "Backup done"
fi

--------------------------------------------------

📂 File Test Operators
--------------------------------------------------

-f → file exists
-d → directory exists
-r → readable
-w → writable
-x → executable

Example:

if [ -f file.txt ]
then
 echo "File exists"
fi

--------------------------------------------------

📦 Backup Script using zip
--------------------------------------------------

Install zip:
sudo apt install zip

Script: backup.sh

#!/bin/bash

date=$(date +%F)
zip backup-$date.zip /home/ubuntu/data/*

echo "Backup completed"

--------------------------------------------------

⏰ Cron Job (crontab)
--------------------------------------------------

Cron is used for scheduling jobs.

Open crontab:
crontab -e

Format:
min hour day month week command

Example (Daily 2 AM):
0 2 * * * /home/ubuntu/backup.sh

Check jobs:
crontab -l

--------------------------------------------------

☁️ AWS S3 (Simple Storage Service)
--------------------------------------------------

S3 is object storage service.

Uses:
• Backup 📦
• Media storage 🎬
• Logs 📝
• Static websites 🌍

Features:
• Unlimited storage
• High durability
• Secure

--------------------------------------------------

📌 Create S3 Bucket
--------------------------------------------------

AWS Console:

1. Open S3
2. Create bucket
3. Give unique name
4. Select region
5. Create

Bucket name example:
my-linux-backups

--------------------------------------------------

🔗 Connect EC2 to S3 (AWS CLI)
--------------------------------------------------

Step 1: Install AWS CLI

sudo apt install awscli

Check:
aws --version

Step 2: Configure

aws configure

Enter:
Access Key
Secret Key
Region
Format

--------------------------------------------------

📤 Upload Files to S3
--------------------------------------------------

Upload file:
aws s3 cp file.zip s3://bucket-name/

Upload folder:
aws s3 cp /data s3://bucket-name/ --recursive

List files:
aws s3 ls s3://bucket-name/

--------------------------------------------------

📥 Download from S3
--------------------------------------------------

aws s3 cp s3://bucket-name/file.zip .

--------------------------------------------------

📦 Backup to S3 Script
--------------------------------------------------

Script: s3backup.sh

#!/bin/bash

date=$(date +%F)

zip backup-$date.zip /home/ubuntu/data/*

aws s3 cp backup-$date.zip s3://my-linux-backups/

echo "Backup uploaded to S3"

--------------------------------------------------

⏰ Auto Backup to S3 using Cron
--------------------------------------------------

Open cron:
crontab -e

Add:

0 1 * * * /home/ubuntu/s3backup.sh

Runs daily at 1 AM ⏳

--------------------------------------------------

🔐 IAM Role Method (Best Practice)
--------------------------------------------------

Instead of keys, use IAM Role.

Steps:
1. Create IAM role with S3 access
2. Attach to EC2
3. AWS CLI auto connects

More secure 🔒

--------------------------------------------------

🧠 Shell Scripting Rules
--------------------------------------------------

✔ Always use shebang  
✔ No spaces in variables  
✔ Use quotes for strings  
✔ Check permissions  
✔ Validate inputs  
✔ Use comments  

--------------------------------------------------

📌 Common Debugging
--------------------------------------------------

Run script in debug mode:
bash -x script.sh

Shows step by step execution 🐞

--------------------------------------------------

🧠 SUMMARY
--------------------------------------------------

✔ Shell scripting = Automation  
✔ /bin/bash = Shell path  
✔ chmod +x = Execute  
✔ if/loop/function = Logic  
✔ zip = Backup  
✔ cron = Scheduler  
✔ S3 = Cloud storage  
✔ awscli = Connect EC2 to S3  
✔ Scripts + Cron = Auto backup  

==================================================
🎉 END OF SHELL SCRIPTING & S3 NOTES 🚀

