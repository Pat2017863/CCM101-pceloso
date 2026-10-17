# Laboratory 09 - Cloud Automation Engineer

## Mission Overview

This laboratory focuses on automating cloud administration tasks using Bash shell scripting and the Linux Cron scheduler. The mission is to create sample application data, automatically compress it into a backup archive, test the script, and configure a daily scheduled backup.

## Objectives

- Understand Bash scripts, variables, and the shebang line.
- Create and execute a Bash backup script.
- Use chmod to grant executable permission.
- Compress application data using tar.
- Configure and verify a Cron job.
- Document the automation process using Markdown.
- Maintain the existing GitHub Cloud Computing Portfolio.

## Commands Executed

| Command | Purpose |
|---|---|
| `mkdir -p` | Create directories if they do not exist. |
| `echo` | Create sample data in a text file. |
| `nano` | Open a terminal text editor. |
| `chmod +x` | Grant executable permission to a script. |
| `./backup.sh` | Execute the backup script. |
| `tar -czf` | Create a compressed archive. |
| `ls -l` | List files and their permissions. |
| `crontab -l` | Display the current Cron schedule. |
| `crontab -e` | Edit the user's Cron schedule. |
| `git add` | Stage changes for a commit. |
| `git commit` | Record changes in Git history. |
| `git push` | Upload committed changes to GitHub. |

## Skills Learned

- Bash scripting and variable usage.
- Linux file permissions and executable scripts.
- File compression and backup verification.
- Cron scheduling for unattended tasks.
- Markdown technical documentation.
- Git and GitHub version control.

## Evidence

Screenshots are stored in the `screenshots/` directory.

- `script-execution.png` - Backup script execution and generated archive.
- `cron-schedule.png` - Installed Cron schedule.
