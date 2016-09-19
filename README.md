macOS Server
=========

Configure macOS Server

Requirements
------------

* SSH access to the server
* `sudo` privileges
* macOS Server application launched at least once

Role Variables
--------------
**macos_srvr_extra_files_dir**    Path where extra files are copied (Default: "/Users/Shared/")

**macos_srvr_config_directory**   Where script templates will be copied (Default:/etc/ansible)

**macos_srvr_hostname**       Name of the server minus domain (not FQDN).

**macos_srvr_domain**         Domain

**macos_srvr_loginbanner**    Text displayed on login screen.

**macos_srvr_network_service**    Named service used for network connectivity. This determines where the IP, DNS, and hostname will be set. You can find available network services by running `networksetup -listallnetworkservices`.

**macos_srvr_timeserver**     FQDN of time server.

**macos_srvr_timezone**       Timezone of time server (Default: GMT)

**macos_srvr_service_state**  Service names and there status that will be passed to `serveradmin`.

**macos_srvr_packages**       List of packages to be installed with Homebrew.


Dependencies
------------



Example Playbook
----------------

    - name: macOS Server
      hosts: osx_server
      sudo: yes

      vars:
        macos_srvr_servername: xserv-1
        macos_srvr_timeserver: ntp.acme.com

      roles:
        - osx_server

License
-------

MIT
