# Backup Script Guide

## 1. Purpose

This guide explains how the CloudNova Technologies backup script works, how executable permissions are configured, and how the Linux Cron scheduler runs the script automatically.

## 2. Complete Bash Script

The script is stored at `/root/backup.sh`.

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="/root/app-data"
BACKUP_DIR="/root/backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

if [ ! -d "$SOURCE_DIR" ]; then
    echo "Error: Source directory does not exist: $SOURCE_DIR"
    exit 1
fi

mkdir -p "$BACKUP_DIR" || exit 1

if tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" -C /root app-data; then
    echo "Backup completed successfully at $TIMESTAMP!"
else
    echo "Error: Backup failed."
    exit 1
fi
```

## 3. Explanation of the Script

- `#!/bin/bash` specifies Bash as the interpreter.
- `SOURCE_DIR` identifies the application data directory.
- `BACKUP_DIR` specifies where the archives are stored.
- `TIMESTAMP` creates a date and time string for the backup filename.
- `mkdir -p` creates the backup directory if it does not exist.
- `tar -czf` compresses the application directory into a `.tar.gz` archive.
- The `if` statements check whether the source directory exists and whether the backup operation succeeds.
- `exit 1` indicates an error when the script cannot complete its task.

The timestamp helps distinguish backup files created at different times. The archive can be inspected using `tar -tzf`.

## 4. Executable Permissions

The command used was:

```bash
chmod +x /root/backup.sh
```

The `chmod` command changes file permissions, and `+x` adds executable permission. This allows the script to be launched directly using `/root/backup.sh`. Without executable permission, a direct attempt to run the script may return a permission-denied error.

## 5. Cron Schedule

The configured Cron expression is:

```cron
0 2 * * * /root/backup.sh
```

The fields have the following meanings:

| Field | Value | Meaning |
|---|---|---|
| Minute | `0` | At minute zero |
| Hour | `2` | At 2:00 AM |
| Day of Month | `*` | Every day of the month |
| Month | `*` | Every month |
| Day of Week | `*` | Every day of the week |

This configuration schedules the backup script to run daily at 2:00 AM, according to the system's local time.

## 6. Testing and Verification

The script was tested manually after executable permission was granted. The generated archive was checked using:

```bash
ls -lh /root/backups/
tar -tzf /root/backups/backup_FILENAME.tar.gz
```

Replace `backup_FILENAME.tar.gz` with the actual archive filename when running the second command.

The expected archive contains the `app-data` directory and its `data.txt` file. The Cron configuration can be checked using `crontab -l`.

## 7. Operational Considerations

This exercise uses sample data in a temporary learning environment. A production backup solution should also consider secure access, sufficient storage, retention policies, monitoring, and copies stored outside the original server. A backup should be tested through restoration, not only by checking whether an archive exists.
