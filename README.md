
# sysopctl - System Operation Command

`sysopctl` is a custom Bash command designed to manage system services, monitor processes, and handle system health tasks in a Linux environment. This project was built to enhance system administration capabilities by offering a simplified, easy-to-use command-line tool.

## Features

- **Service Management**: Start, stop, and list services.
- **System Load Monitoring**: View system load averages.
- **Disk Usage Monitoring**: Check disk usage by partitions.
- **Process Monitoring**: View real-time process activity.
- **Log Analysis**: Analyze critical system logs.
- **File Backup**: Perform system file backups using `rsync`.

## Installation

To install and use `sysopctl`, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Kanak2025/sysopctl.git
   cd sysopctl
   ```

2. **Make the Script Executable**:
   ```bash
   chmod +x sysopctl
   ```

3. **(Optional) Move the Script to a Directory in Your PATH**:
   This allows you to run `sysopctl` from anywhere in your terminal.
   ```bash
   sudo mv sysopctl /usr/local/bin/
   ```

## Usage

Here’s how to use `sysopctl`:

1. **Help**: Display available commands and options:
   ```bash
   sysopctl --help
   ```
   ![help](https://github.com/user-attachments/assets/92cb6bdc-d8ff-4318-8ece-d73a9b76f7ea)

   
2. **Version**: Display the current version of `sysopctl`:
   ```bash
   sysopctl --version
   ```
   ![version](https://github.com/user-attachments/assets/0773f771-2352-4e07-b753-455d7b8ee64d)


3. **List Running Services**: Show all active services (similar to `systemctl list-units --type=service`):
   ```bash
   sysopctl service list
   ```
   ![services](https://github.com/user-attachments/assets/20c21313-1570-49ec-b9ae-21e851a356d3)

   

4. **Start a Service**: Start a specific service (similar to `systemctl start`):
   ```bash
   sysopctl service start <service-name>
   ```
   ![service start](https://github.com/user-attachments/assets/de33e10b-de80-4af9-9ad1-f7603e740c3b)


5. **Stop a Service**: Stop a specific service (similar to `systemctl stop`):
   ```bash
   sysopctl service stop <service-name>
   ```
   ![service stop](https://github.com/user-attachments/assets/3486869a-0d97-4606-a7ba-2c4bddd78510)


6. **Check Disk Usage**: Show disk usage by partitions (similar to `df -h`):
   ```bash
   sysopctl disk usage
   ```
   ![disk](https://github.com/user-attachments/assets/7028b511-3d59-4a1d-82a7-c3d9b03f51b6)


7. **Monitor Processes**: Display real-time process activity (similar to `top`):
   ```bash
   sysopctl process monitor
   ```
   ![monitor](https://github.com/user-attachments/assets/c02323d1-bd74-46b0-812a-3c7d92a6a6f3)


8. **Analyze Logs**: Analyze recent critical system logs (using `journalctl`):
   ```bash
   sysopctl logs analyze
   ```
   ![logs](https://github.com/user-attachments/assets/79e09295-0343-49e2-b4fe-2c18302fdd4a)


9. **Backup Files**: Perform a system file backup using `rsync`:
   ```bash
   sysopctl backup <path-to-backup>
   ```
   ![backup](https://github.com/user-attachments/assets/ebb1e922-b781-4850-8ff1-d2e0d74c2e90)

   ![manpage](https://github.com/user-attachments/assets/18108255-9d8f-4d1a-bde0-0321585bca1d)

   ![versioncntrl](https://github.com/user-attachments/assets/2e42d437-a5a8-412a-bccb-d31930f4df8b)


## Example

Here’s an example of how to start the `cron` service using `sysopctl`:

```bash
sysopctl service start cron
```

And an example to check disk usage:

```bash
sysopctl disk usage
```

## Requirements

- **Bash Shell**: `sysopctl` is a Bash script and requires a Bash shell environment.
- **Systemd**: The service management feature relies on `systemctl`, which is available on systemd-based Linux distributions.
- **Rsync**: Required for the backup feature.

 
