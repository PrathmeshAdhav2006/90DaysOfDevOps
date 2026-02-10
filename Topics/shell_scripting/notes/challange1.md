# Week 3 Bash Scripting Challenges

This document contains solutions for:

1. User Account Management Script
2. Automated Backup with Rotation Script

---

# ✅ Challenge 1: User Account Management Script

## File: user_management.sh

```bash
#!/bin/bash

# ==========================================
# User Account Management Script
# ==========================================
# This script allows:
# - Create users
# - Delete users
# - Reset passwords
# - List users
# - Show help
#
# NOTE: Must be run as root or with sudo
# ==========================================

# Check if script is run as root
if [ "$EUID" -ne 0 ]; then
  echo "Please run as root (use sudo)"
  exit 1
fi

# Function to display help
show_help() {
  echo "User Management Script"
  echo "Usage: ./user_management.sh [OPTION]"
  echo ""
  echo "Options:"
  echo "  -c, --create     Create new user"
  echo "  -d, --delete     Delete existing user"
  echo "  -r, --reset      Reset user password"
  echo "  -l, --list       List all users"
  echo "  -h, --help       Show help"
}

# Function to check if user exists
user_exists() {
  id "$1" &>/dev/null
}

# Create User
create_user() {

  read -p "Enter new username: " username

  if user_exists "$username"; then
    echo "User '$username' already exists!"
    exit 1
  fi

  read -s -p "Enter password: " password
  echo
  read -s -p "Confirm password: " confirm
  echo

  if [ "$password" != "$confirm" ]; then
    echo "Passwords do not match!"
    exit 1
  fi

  useradd -m "$username"
  echo "$username:$password" | chpasswd

  echo "User '$username' created successfully."
}

# Delete User
delete_user() {

  read -p "Enter username to delete: " username

  if ! user_exists "$username"; then
    echo "User '$username' does not exist!"
    exit 1
  fi

  userdel -r "$username"

  echo "User '$username' deleted successfully."
}

# Reset Password
reset_password() {

  read -p "Enter username: " username

  if ! user_exists "$username"; then
    echo "User '$username' does not exist!"
    exit 1
  fi

  read -s -p "Enter new password: " password
  echo
  read -s -p "Confirm password: " confirm
  echo

  if [ "$password" != "$confirm" ]; then
    echo "Passwords do not match!"
    exit 1
  fi

  echo "$username:$password" | chpasswd

  echo "Password reset successful for '$username'."
}

# List Users
list_users() {

  echo "Username : UID"
  echo "----------------"

  awk -F: '{print $1 " : " $3}' /etc/passwd
}

# Main Logic
case "$1" in

  -c|--create)
    create_user
    ;;

  -d|--delete)
    delete_user
    ;;

  -r|--reset)
    reset_password
    ;;

  -l|--list)
    list_users
    ;;

  -h|--help)
    show_help
    ;;

  *)
    echo "Invalid option!"
    show_help
    ;;

esac




✅ Challenge 2: Automated Backup with Rotation
File: backup_with_rotation.sh

#!/bin/bash

# ==========================================
# Backup with Rotation Script
# ==========================================
# This script:
# - Creates timestamped backups
# - Keeps only last 3 backups
# ==========================================

# Check argument
if [ $# -ne 1 ]; then
  echo "Usage: ./backup_with_rotation.sh <directory>"
  exit 1
fi

SOURCE_DIR="$1"

# Check if directory exists
if [ ! -d "$SOURCE_DIR" ]; then
  echo "Directory does not exist!"
  exit 1
fi

# Create timestamp
TIMESTAMP=$(date +"%Y-%m-%d_%H-%M-%S")

BACKUP_DIR="$SOURCE_DIR/backup_$TIMESTAMP"

# Create backup folder
mkdir "$BACKUP_DIR"

# Copy files
cp -r "$SOURCE_DIR"/* "$BACKUP_DIR" 2>/dev/null

echo "Backup created: $BACKUP_DIR"

# Get list of backup folders (sorted)
BACKUPS=$(ls -dt "$SOURCE_DIR"/backup_* 2>/dev/null)

# Count backups
COUNT=$(echo "$BACKUPS" | wc -l)

# Remove old backups if more than 3
if [ "$COUNT" -gt 3 ]; then

  REMOVE=$(echo "$BACKUPS" | tail -n +4)

  for folder in $REMOVE; do
    rm -rf "$folder"
    echo "Removed old backup: $folder"
  done

fi





How To Use
Make Scripts Executable
chmod +x user_management.sh
chmod +x backup_with_rotation.sh

Run User Management
sudo ./user_management.sh -c   # Create user
sudo ./user_management.sh -d   # Delete user
sudo ./user_management.sh -r   # Reset password
sudo ./user_management.sh -l   # List users
sudo ./user_management.sh -h   # Help

Run Backup Script
./backup_with_rotation.sh /path/to/directory
