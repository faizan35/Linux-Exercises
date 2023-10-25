# 1. Automated Backup Script

_Welcome to the Automated Backup Script exercise! This project is designed to help you create a script that automates the backup of important files and directories on a Linux system._

## Exercise Description

Your task is to develop a shell script that performs the following:

1. **File Selection:**

   - Allow users to specify files and directories to be included in the backup.

2. **Backup Destination:**

   - Provide an option to choose the destination directory where the backup will be stored.

3. **Timestamping:**

   - Add a timestamp to the backup files for easy tracking of when the backup was performed.

4. **Automation:**
   - Implement a scheduling mechanism (using tools like cron) to automate the backup process at regular intervals.

## Instructions for Creating Files and Directories

To ensure consistency among participants, let's first create the necessary files and directories:

Open your terminal and execute the following commands:

```bash
mkdir backup_script_exercise

mkdir project-dir
cd project-dir

mkdir A-project B-project C-project D-project E-project
touch A-project/project-info-A.txt
touch B-project/project-info-B.txt
touch C-project/project-info-C.txt
touch D-project/project-info-D.txt
touch E-project/project-info-E.txt
```

Now, let's move on to the main task.

# Challenge

Automate backups for **A-project/** to **E-project/** dir with unique schedules corresponding to the **challenge no A to E**:

**A)** _Create a backup every 6 hours._
**B)** _Schedule a backup every day._
**C)** _Perform a backup every 5 minutes._
**D)** _Create a weekly backup._
**E)** _Schedule a backup every month._

# Hints

To get started, consider the following commands and concepts:

- `tar` command for creating and extracting tar archives.
- `cp` command for copying files and directories.
- `date` command for generating timestamps.
- `crontab` for scheduling recurring tasks.
- `chmod +x script.sh` make the Script Executable

Feel free to explore additional Linux commands and options to enhance your script.

# Solution

The solution for this exercise can be found in the [solution.md](./solution.md) file. Before checking the solution, try to implement the script on your own.

Happy coding!

[Next Exercise →](../2-System-Monitoring-Tool/README.md)
