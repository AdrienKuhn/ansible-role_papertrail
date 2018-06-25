Papertrail
==========

This role will install and configure Papertrail with remote_syslog

Requirements
------------

None

Supported distributions
-----------------------

- Debian:
    - 8 (Jessie)
    - 9 (Stretch)

Configuration
-------------

```
papertrail:
  dst:
    host: CHANGE_ME
    port: CHANGE_ME
  files:
    - /var/log/nginx/*.log
    - /var/log/letsencrypt/*.log
  remote_syslog: true
  exclude_patterns:
    - dont log this pattern
```

Dependencies
------------

None

Tests
-----

```
$ cd tests
$ vagrant up --provision
```