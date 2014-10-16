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

    - name: OS X Server
      hosts: osx_server
      sudo: yes

      vars:
        osxs_servername: xserv-1
        osxs_timeserver: ntp.acme.com

      roles:
        - osx_server

License
-------

MIT
