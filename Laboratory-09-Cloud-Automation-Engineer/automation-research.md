# Research: The Language of Automation

## 1. Bash Script

A Bash script is a text file containing commands that the Bash shell can execute in sequence. It helps automate repetitive tasks, such as creating folders, backing up files, and checking system information. The line `#!/bin/bash` is called the shebang, and it tells the operating system to use Bash to interpret the script when it is executed directly.

## 2. Variables

Variables store values that a script can reuse, such as directory paths, filenames, and timestamps. For example, `$BACKUP_DIR` represents the backup directory stored in the `BACKUP_DIR` variable. Using variables makes scripts easier to update because a value can be changed in one place instead of editing every command that uses it.

## 3. Cron Job

A Cron job is a scheduled task managed by the Linux Cron service. It allows commands or scripts to run automatically at specified times without requiring someone to start them manually. Cron is important in cloud operations because it can schedule routine work, such as backups and maintenance, consistently and reliably.
