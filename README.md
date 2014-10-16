OS X Server
=========

Configure OS X Server

Requirements
------------

* SSH access to the server
* `sudo` privileges

Role Variables
--------------
**osxs_servername**     Name of the server (not FQDN).

**osxs_timeserver**     FQDN of time server.

**osxs_timezone**       Timezone of time server (Default: GMT)

**osxs_systemsetup**    Hash of commands and parameters sent to `systemsetup` command.

**osxs_serveradmin**    Hash of commands sent to `serveradmin` command.

**osxs_packages**       List of packages to be installed with Homebrew.


Dependencies
------------



Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

MIT
