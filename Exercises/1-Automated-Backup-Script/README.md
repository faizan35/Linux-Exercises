# 1. Automated Backup Script

_Welcome to the Automated Backup Script exercise! This project is designed to help you create a script that automates the backup of important files and directories on a Linux system._

## Exercise Description

Your task is to develop a shell script that performs the following:

1. **File Archiving & Compression:**

   - Archive the directory, and then create a backup using tools like tar and gzip..

2. **Timestamping:**

   - Add a timestamp to the backup files for easy tracking of when the backup was performed.

3. **Automation:**
   - Implement a scheduling mechanism (using tools like cron) to automate the backup process at regular intervals.

## Instructions for Creating Files and Directories

To ensure consistency among participants, let's first create the necessary files and directories:

Open your terminal and execute the following commands:

```bash
mkdir backups
cd backups
mkdir {A..E}-pro-backup
```

```bash
mkdir scripts
cd scripts

touch {A..E}-pro-backup.sh
```

```bash
mkdir project-dir
cd project-dir

mkdir {A..E}-project
touch {A..E}-project/project-info.txt  # Create's txt file inside A-project/ to E-project dir.
```

**Note :-** **backups**, **scripts** & **project-dir** directories are on the same level.

## Challenge's

1. _Create a backup every 6 hours._ **=>** On `A-project/` dir
2. _Schedule a backup every day at 12:00AM._ **=>** On `B-project/` dir
3. _Perform a backup every 5 minutes._ **=>** On `C-project/` dir
4. _Create a weekly backup every Wednesday at 5:00PM._ **=>** On `D-project/` dir
5. _Schedule a backup every month on 27th date at 7:30PM._ **=>** On `E-project/` dir
6. Create a log file for cron job taking backup in challeng-3. **=>** On `C-project/` dir

## Hints

To get started, consider the following commands and concepts:

- `tar` command for creating and extracting tar archives.
- `cp` command for copying files and directories.
- `date` command for generating timestamps.
- `crontab` for scheduling recurring tasks.
- `chmod +x script.sh` make the Script Executable

Feel free to explore additional Linux commands and options to enhance your script.

## Solution & Theory

The solution for this exercise can be found in the [Solution](./solution.md) file and detailed theory about the commands [Theory](./theory.md) file Before checking the solution, try to implement the script on your own.

Happy coding!

[Next Exercise →](../2-System-Monitoring-Tool/README.md)
