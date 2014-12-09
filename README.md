OS X Server
=========

Configure OS X Server

Requirements
------------

* SSH access to the server
* `sudo` privileges
* OS X Server application launched at least once

Role Variables
--------------
**osxs_extra_files_dir**    Path where extra files are copied (Default: "/Users/Shared/")

**osxs_config_directory**   Where script templates will be copied (Default:/etc/ansible)

**osxs_hostname**       Name of the server minus domain (not FQDN).

**osxs_domain**         Domain

**osxs_loginbanner**    Text displayed on login screen.

**osxs_network_service**    Named service used for network connectivity. This determines where the IP, DNS, and hostname will be set. You can find available network services by running `networksetup -listallnetworkservices`.

**osxs_timeserver**     FQDN of time server.

**osxs_timezone**       Timezone of time server (Default: GMT)

**osxs_service_state**  Service names and there status that will be passed to `serveradmin`.

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
