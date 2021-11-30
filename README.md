BACKUP Ansible role
==================

Role to manage BACKUP. This backup mechanism create a copy of tgz files into a specific local
directory, then eventually mirror it on a sFTP server.

Requirements
------------

No requirements

Role Variables
--------------

`backup__install` For install only (default: False)
`backup__configure` For configuration  (default: False)
`backup__mysql` Include MySQL backup process (default: False)

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
