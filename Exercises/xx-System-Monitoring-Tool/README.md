# System Monitoring Tool

_Welcome to the System Monitoring Tool exercise! In this project, you'll create a tool to monitor various system resources on a Linux system._

## 1. Exercise Description

Your task is to develop a script or tool that performs the following monitoring tasks:

1. **CPU Usage:**

   - Display the current CPU usage, and if possible, break it down by individual cores.

2. **Memory Usage:**

   - Show the current memory usage, including total, used, and free memory.

3. **Disk Space:**

   - Provide information on disk space usage, highlighting the available space on each mounted partition.

4. **Network Activity:**
   - Display network-related information, such as active connections and data transfer rates.

## 2. Instructions for Creating Files and Directories

To maintain consistency across participants, let's set up the necessary files and directories:

1. Create a directory named `sys-monitor-tool`.
   ```bash
   mkdir sys-monitor-tool
   cd sys-monitor-tool
   ```

## 3. Challenges

##### 1. **CPU Profiling with Sar**

- **Objective**: Implement continuous monitoring of CPU usage.
- **Challenge**: Set up the System Activity Reporter (`sar`) to collect and display CPU utilization data at 10-second intervals. Extract and analyze the CPU usage trends over a 5-minute duration.

- **Hint**: Use `sar -u` to display CPU utilization, and explore options like `-o` to save the data to a file for analysis.

##### 2. Memory Analysis with vmstat

- **Objective**: Gain insights into memory performance.

- **Challenge**: Use `vmstat` to display statistics about system memory usage, including swap space. Identify the memory usage patterns and observe the impact on the system during a simulated memory-intensive task.

- **Hint**: Run `vmstat` with a time interval (e.g., `vmstat 5`) to display memory statistics at regular intervals.

##### 3. Disk Space Monitoring with iostat

- **Objective**: Monitor disk I/O activities.

- **Challenge**: Utilize `iostat` to monitor disk I/O statistics, including read and write operations. Identify the disk with the highest I/O activity and analyze the patterns over a 10-minute period.

- **Hint**: Use `iostat -d` to display disk I/O statistics.

##### 4. Network Monitoring with nload

- **Objective**: Monitor network bandwidth in real-time.

- **Challenge**: Install and use `nload` to monitor incoming and outgoing network traffic. Identify the network interface with the highest bandwidth usage and observe the variations over a 5-minute duration.

- **Hint**: Install `nload` and run it with the desired network interface (e.g., `nload eth0`).

<!-- ##### 5. Custom Alerts with Monit

- **Objective**: Set up automated alerts for critical system conditions.

- **Challenge**: Install and configure `monit` to monitor CPU usage, memory, and disk space. Create custom alerts to notify you when any of these metrics exceed predefined thresholds. Test the alerts by triggering simulated resource-intensive tasks.

- **Hint**: Use `monit` configuration files to define monitoring rules and actions. -->

##### 5. Custom Resource Logging with SystemTap

- **Objective**: Create a custom script to monitor a specific system resource and redirect the output to a file.

- **Challenge**: Use SystemTap to create a script that monitors a custom resource of your choice (e.g., file I/O, specific process activity, etc.). Redirect the output of the script to a log file, and analyze the data for patterns or anomalies over a 10-minute duration.

- **Hint**: Explore SystemTap scripts, and use redirection (> or >>) to save the output to a file.

## 4. Hints

- `sar` for CPU profiling.
- `vmstat` for memory analysis.
- `iostat` for disk space monitoring.
- `nload` for network monitoring.
- `monit` for creating custom alerts.
- `SystemTap` for custom resource logging.

## 5. Solution

The solution for this exercise can be found in the [Solution](./solution.md) file and detailed theory about the commands [Theory](./theory.md) file Before checking the solution, try to implement the script on your own.

Happy coding!

← [Previous Exercise](../1-Automated-Backup-Script/README.md) | [Next Exercise →](../3-Package-Manager-Simulator/README.md)
