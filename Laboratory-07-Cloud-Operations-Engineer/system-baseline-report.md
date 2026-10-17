# System Baseline Report

## 1. Purpose

The purpose of this report is to check the health of the Linux host before deploying the client's web server. This helps ensure that the server has enough memory, disk space, and CPU resources to run the application properly.

## 2. Memory Check

**Command executed:** `free -h`

- **Total RAM:** 1.9 GiB
- **Used RAM:** 444 MiB
- **Free RAM:** 890 MiB
- **Available RAM:** 1.4 GiB
- **Swap Total:** 1.0 GiB
- **Swap Used:** 0 B

The memory check shows that the server has 1.9 GiB of RAM, with 1.4 GiB available for applications and other processes. No swap space is currently being used.

## 3. Disk Check

**Command executed:** `df -h /`

- **Root filesystem:** `/dev/vda1`
- **Root filesystem size:** 19 GiB
- **Used storage:** 5.7 GiB
- **Available storage:** 13 GiB
- **Usage percentage:** 31%
- **Mount point:** `/`

The disk check shows that the root filesystem has a total capacity of 19 GiB, with 13 GiB available. The server is currently using 31% of its disk capacity.

## 4. CPU and Process Monitoring

**Command executed:** `top`

The command displayed the running processes and current CPU activity of the Linux server. It allowed me to observe how system resources were being used while the server was running.

## 5. Why Disk Monitoring Is Important

Checking disk space is important before a traffic surge because the server needs enough storage for application logs, temporary files, and other data. If the disk becomes full, the application may experience errors or stop working correctly.

## 6. Conclusion

The host's memory, disk capacity, and CPU activity were checked to establish a baseline before deploying the Nginx container. The server has 1.9 GiB of RAM and 13 GiB of available disk space. These checks help identify possible resource problems and prepare the server to handle application traffic more reliably.


