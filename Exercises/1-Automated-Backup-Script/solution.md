# Automated Backup Script - Solution

## Pre-Challenge Setup

Before starting the Automated Backup Script exercise, let's set up the necessary directory structure and files. Execute the commands.

After creating you directory structure will look like this:-

```bash
- 1-Automated-Backup-Script
  |- backups
  |   |- A-pro-backup
  |   |- B-pro-backup
  |   |- C-pro-backup
  |   |- D-pro-backup
  |   |- E-pro-backup
  |
  |- scripts
  |   |- A-pro-backup.sh
  |   |- B-pro-backup.sh
  |   |- C-pro-backup.sh
  |   |- D-pro-backup.sh
  |   |- E-pro-backup.sh
  |
  |- project-dir
      |- A-project
      |   |- project-info.txt
      |
      |- B-project
      |   |- project-info.txt
      |
      |- C-project
      |   |- project-info.txt
      |
      |- D-project
      |   |- project-info.txt
      |
      |- E-project
          |- project-info.txt

```

### Challenge 1: Create a backup every 6 hours.

#### Step 1: Write into script file `scripts/A-pro-backup.sh`

```bash
#!/bin/bash

# Change your working dir to A-project/
cd /home/<your_user_name>/1-Automated-Backup-Script/project-dir/A-project/

# Create a compressed file with time-stamp
timestamp=$(date +\%d-\%m-\%Y_\%H_\%M_\%S)

tar -cvzf A-backup_$timestamp.tar.gz *

mv *.gz /home/<your_user_name>/1-Automated-Backup-Script/backups/A-pro-backup/
```

#### Step 2: Ensure that `A-pro-backup.sh` is executable by running:

```bash
chmod u+x /path/to/scripts/A-pro-backup.sh
```

#### Step 3: Setup `cron job`

1. Open the `crontab` file for editing:
   ```bash
   crontab -e
   ```
2. Add your cron entry. For example, to run your backup script every 6 hours:
   ```bash
   0 */6 * * * /path/to/scripts/A-pro-backup.sh
   ```

**Challenge 1 completed.**

#### Tips & Tricks

This will write all the content of `A-pro-backup.sh` to all the files.

```bash
cat A-pro-backup.sh >> B-pro-backup.sh C-pro-backup.sh D-pro-backup.sh E-pro-backup.sh
```

### Challenge 2: Schedule a backup every day at 12:00AM.

#### Step 1: Open `B-pro-backup.sh` in `vim` edittor.

##### To Search and Replace in `vim editor`

- Make sure you are in normal mode by pressing `Esc`.
- Type `:%s/old_pattern/new_pattern/gc` and press `Enter`.
- The cursor will jump to the first occurrence of `old_pattern` in the file. Vim will then show you the line where the match is found, and it will be highlighted.
- At this point, you have several options:
  - `y` : This means **"yes"** and Vim will replace, "old_pattern" with "new_pattern."
  - `n` : This means **"no"** and Vim will skip, without replacement.
  - `a` : This means **"all"** and Vim will replace all remaining occurrences without confirmation.
  - `q` : This means **"quit"** Vim will stop and exit.
  - `l` : This means **"last"** Vim will replace the current occurrence and then stop.
  - `^E` : This means **"scroll line up"** It is only for navigation option.
  - `^Y` : This means **"scroll line down"** Like `^E`, it's for navigation.

```bash
:%s/A/B/gc
```

After replacing A to B `B-pro-backup.sh` looks like.

```bash
#!/bin/bash

# Change your working dir to B-project/
cd /home/<your_user_name>/1-Automated-Backup-Script/project-dir/B-project/

# Create a compressed file with time-stamp
timestamp=$(date +\%d-\%m-\%Y_\%H_\%M_\%S)

tar -cvzf backup_$timestamp.tar.gz *

mv *.gz /home/<your_user_name>/1-Automated-Backup-Script/backups/B-pro-backup/
```

#### Step 2: _Same as Challenge 1_

#### Step 3: Setup `cron job`

1. To run every day at 12:00AM.
2. Add your cron entry. For example, to run your backup script every 6 hours:

```bash
0 20 * * * /path/to/scripts/B-pro-backup.sh
```

**Challenge 2 completed.**

### Challenge 3: Schedule a backup every 5 minutes.

#### Step 1: Same as Challenge 2

#### Step 2: Same as Challenge 2

#### Step 3: Setup `cron job`

1. To run every 5 minutes.
2. Add your cron entry:

```bash
*/5 * * * * /path/to/scripts/C-pro-backup.sh
```

**Challenge 3 completed.**

### Challenge 4: Schedule a backup Weekly every Wednesday at 5:00PM.

#### Step 1: Same as Challenge 2

#### Step 2: Same as Challenge 2

#### Step 3: Setup `cron job`

1. To run every week at 5:00PM.
2. Add your cron entry:

```bash
0 17 * * 3 /path/to/scripts/D-pro-backup.sh
```

**Challenge 4 completed.**

### Challenge 5: Schedule a backup every month on 27th date at 7:30PM.

#### Step 1: Same as Challenge 2

#### Step 2: Same as Challenge 2

#### Step 3: Setup `cron job`

1. To run every month on 27th date at 7:30PM.
2. Add your cron entry:

```bash
30 19 27 * * /path/to/scripts/E-pro-backup.sh
```

**Challenge 5 completed.**

### Challenge 6: Creating log file for cron job running for challenge 3.

_Log files helps you to Redirect the output (stdout and stderr) to a log file within your script._

#### Step 1: Create the logfile.

```bash
cd C-pro-backup/
touch logfile.log
```

#### Step 2: Update `crontab`

```bash
*/5 * * * * /path/to/scripts/C-pro-backup.sh >> /path/to/logfile.log 2>&1
```

**Note :-** _Always give absolute path (i.e. from root)._

**Challenge 6 completed.**
