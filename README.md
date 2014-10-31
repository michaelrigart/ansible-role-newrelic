Ansible NewRelic Role
=====================

An ansible role for installing and configuring NewRelic.
 
For more information, [visit the NewRelic website](http://newrelic.com/)

Role Variables
--------------

- newrelic_license_key: your New Relic license key
- newrelic_pkg_state: indicates the package state; Allowed setting: installed, latest
- newrelic_pkg_version: specify the specific package version you wish to install
When specifying a version, the state will be forced to installed. When omitting the variable or leaving it empty
it will install the package as specified by the state variable 
- newrelic_service_state: indicates the service state; Allowed setting: started, stopped 
- newrelic_service_enabled: indicates if service needs to be enabled on boot; Allowed settings: yes, no
- newrelic_loglevel: New Relic log level; Allowed settings: error, warning, info, verbose, debug, verbosedebug
- newrelic_logfile: Location of New Relic log file
- newrelic_proxy: New Relic proxy address
- newrelic_ssl: Use SSL for communication to New Relic
- newrelic_ssl_ca_bundle: SSL CA Bundle path when using SSL
- newrelic_ssl_ca_path: SSL CA path when using SSL
- newrelic_pidfile: New Relic Pid file location
- newrelic_collector_host: New Relic Collector hostname
- newrelic_timeout: Connection timeout for collector host

View the default vars - defaults/main.yml - for a more detailed example.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: MichaelRigart.newrelic }

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>