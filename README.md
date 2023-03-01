# Rclone Service File (Unit File)

This file is taken from [animosity22/homescripts](https://github.com/animosity22/homescripts/blob/master/systemd/rclone-drive.service) and some changes were made on it, i.e., simplified.

## File Location

**rclone.service** file needs to be put under ``/etc/systemd/system/``.

## Start Rclone Daemon

To start daemon, ``systemctl start rclone.service``. If it works, then ``systemctl enable rclone.service``. 

## Placeholders in *rclone.service* file

* **``<your_remote_name>``**: to find out your remote name, type ``rclone listremotes``.
* **``<username>``** : just type ``whoami``.
* **``</path/to/config/file>``** : 
  * If you don't have config file, you need to create it with ``rclone config`` command.
  * If the default path, ***/home/\<username>\/.config/rclone/rclone.conf***, does not work, locate *the rclone config file* by entering ``rclone config file``.
