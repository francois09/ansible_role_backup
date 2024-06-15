BACKUP Ansible role
==================

Role to manage BACKUP. This backup mechanism create a copy of tgz files into a specific local
directory, then eventually mirror it on a sFTP server.

This role is adapted to Online FTP backup mechanism, but can be easily configured for other host provider mechanisms.

It backups users (home collected into `/etc/passwd` file), `{{ backup__zones }}` and eventually mysql databases.

Requirements
------------

No requirements

Role Variables
--------------

* `backup__install` For install only (default: False)
* `backup__configure` For configuration  (default: False)
* `backup__mysql` Include MySQL backup process (default: False)
* `backup__zones` List of directories to backup (default: { "/root", "/etc" } )
* `backup__retentions` Policy for keeping backups. List of `zone:duration` (default: { "*:2W", "mysql:2W", "users:2W" } )
* `backup__exclude` File format exclusion. List of templates like "*nologin*" or "*/com_joomlapack/backup/*"
* `backup__mirror` Boolean to activate mirroring on FTP server
* `backup__mirror_host` FTP Hostname
* `backup__mirror_user` FTP User
* `backup__mirror_pass` FTP Password

* `backup__mirror_hour`, `backup__mirror_min` for mirror cron time
* `backup__cleaner_hour`, `backup__cleaner_min` for cleaner cron time


Dependencies
------------

None

Example Playbooks
-----------------

License
-------

GPL v3

Author Information
------------------

François TOURDE
