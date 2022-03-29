RClone Manager
============================

RClone Manager extension for Gnome-Shell - Adds a rclone indicator to the top panel in roder to manage rclone configurations.

# Features 

- Adds an indicator in the system tray to check and manage rclone configurations
- Works with rclone
- Cutomizable rclone commands
- Two modes of work: watch files and mount remote service
- Potentialy compatible with those cloud services: 1Fichier, Akamai Netstorage, Alibaba Cloud (Aliyun) Object Storage System (OSS), Amazon Drive (See note), Amazon S3, Backblaze B2, Box, Ceph, Citrix ShareFile, C14, DigitalOcean Spaces, Digi Storage, Dreamhost, Dropbox, Enterprise File Fabric, FTP, Google Cloud Storage, Google Drive, Google Photos, HDFS, HTTP, Hubic, Jottacloud, IBM COS S3, Koofr, Mail.ru Cloud, Memset Memstore, Mega, Memory, Microsoft Azure Blob Storage, Microsoft OneDrive, Minio, Nextcloud, OVH, OpenDrive, OpenStack Swift, Oracle Cloud Storage, ownCloud, pCloud, premiumize.me, put.io, QingStor, Rackspace Cloud Files, rsync.net, Scaleway, Seafile, Seagate Lyve Cloud, SeaweedFS, SFTP, Sia, StackPath, Storj, SugarSync, Tencent Cloud Object Storage (COS), Uptobox, Wasabi, WebDAV, Yandex Disk, Zoho WorkDrive, The local filesystem 
- It has been tested on Dropbox, Gdrive and OneDrive. Other compatible cloud services may (not) work (see rclone docum), hope you enjoy trying them

## Features of watch mode

- Sycronices file downstream from cloud on start (see rclone sync docum)
- Does monitor local files and keeps them in sync with cloud storage
- Files are stored locally, you will be able to access them offline (offline changes will be lost on manual sync)
- System tray icon show the sync status for easy check, system notifications show eventual errors
- No loops or CPU consumiption when idle

## Features of mount mode

- Updates files with remote modifications, no sync needed
- Will not consume local disk space

# Limitations
# DISCLAIMER

- This program could delete all your files recursively, files backup is strongly advised
- Absolutely no warranty, use under you own risk

## Limitations of watch Mode

- Does not monitor cloud services, and will not update local files with remote modifications "live", manual sync is needed
- local offline changes will be losts on manual sync, allways check your changes have synched successfully

## Limitations of mount model

- Files are not stored locally, internet connection needed
- It is slow to work with files in this mode



Extension page on e.g.o:
https://extensions.gnome.org/extension/xxx

Debugging

make install && make run 2>&1 | grep -i -e RClone

	

To Debug the Extension (extension.js), use this in terminal:
journalctl -f -o cat /usr/bin/gnome-shell

To Debug the Extension Preferences (prefs), use this in terminal:
journalctl -f -o cat /usr/bin/gnome-shell-extension-prefs



Installation
----------------

Installation via git is performed by cloning the repo into your local gnome-shell extensions directory (usually ~/.local/share/gnome-shell/extensions/)::

    $ git clone https://github.com/germanztz/gnome-shell-extension-rclone-manager <extensions-dir>/rclone-manager@daimler.com

After cloning the repo, the extension is practically installed yet disabled. In
order to enable it, you need to use gnome-tweak-tool - find the extension,
titled 'RClone Manager', in the 'Extensions' screen and turn it 'On'.
You may need to restart the shell (Alt+F2 and insert 'r' in the prompt) for the
extension to be listed there.

Doc

https://gjs.guide/

https://gjs-docs.gnome.org

https://wiki.gnome.org/

https://www.codeproject.com/Articles/5271677/How-to-Create-A-GNOME-Extension

https://github.com/julio641742/gnome-shell-extension-reference