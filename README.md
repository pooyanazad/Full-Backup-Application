# Backup
Full Backup Script</br>
```
apt install git
git clone https://github.com/pooyanazad/Backup.git
chmod +x backup.sh
```
You should change below information with your requests in "config.sh" file</br>
- set your backup source
- set your backup destination
- set your backup log path
- set your backup saving days
- set your backup compressing level</br>

```
./backup.sh or use it on crontab like me : 5 0 * * * /mnt/backup.sh
```

This application is my production daily backup script and it will keep your last 5 days backup also added some function to keep every 15th of month backup for 2 years as a monthly backup</br>
</br>
I want to add some fetures to this script with your help and idea:</br>

- Add email part to sent notification if process goes fail (we can use and API or some linux package and send directly), I defined that as an issue and you can help to solve it.
- **Email Notifications for Failures**:
  - The script can now send an email notification if the backup process encounters an error.
  - To enable this, configure the following variables in `config.sh`:
    - `recipient_email="your_email@example.com"`: The email address to send failure alerts to.
    - `sender_email="backup-script@yourdomain.com"`: The "From" address for the notification email. (Note: Your mail server might need configuration to allow sending from this address).
    - `email_subject_failure="BACKUP FAILED"`: The subject line for the failure email.
  - **Dependency**: This feature requires a command-line mail utility to be installed on your system, such as `mailutils` (which provides the `mail` command). You can typically install it using your system's package manager (e.g., `sudo apt install mailutils`).
- You can share your idea!</br>
</br>
You can find me: Pooyan.azadparvar@gmail.com </br>
