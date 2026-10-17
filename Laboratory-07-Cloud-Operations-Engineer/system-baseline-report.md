# System Baseline Report

## 1. Purpose

The purpose of this report is to check the health of the Linux host before deploying the client's web server.

## 2. Memory Check

Command executed:

`free -h`

- Total RAM: [Enter the total RAM shown in your terminal]
- Used RAM: [Enter the used RAM]
- Available RAM: [Enter the available RAM]

## 3. Disk Check

Command executed:

`df -h /`

- Root filesystem size: [Enter the Size value]
- Used storage: [Enter the Used value]
- Available storage: [Enter the Avail value]
- Usage percentage: [Enter the Use% value]

## 4. CPU and Process Monitoring

Command executed:

`top`

The command displayed the running processes and current CPU activity of the Linux server.

## 5. Why Disk Monitoring Is Important

Checking disk space is important before a traffic surge because the server needs enough storage for application logs, temporary files, and other data. If the disk becomes full, the application may experience errors or stop working correctly.

## 6. Conclusion

The host's memory, disk capacity, and CPU activity were checked before deploying the Nginx container.
