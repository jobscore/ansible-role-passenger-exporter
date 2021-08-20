[![Build Status](https://travis-ci.org/jobscore/ansible-role-passenger-exporter.svg?branch=master)](https://travis-ci.org/github/jobscore/ansible-role-passenger-exporter)

Prometheus Passenger Exporter role
=========

An Ansible role for installing Prometheus Passenger Exporter on a Ubuntu box.
This role is based on https://github.com/jobscore/passenger_exporter

Requirements
------------

Passenger must be already installed.

Role Variables
--------------

```
prometheus_passenger_nginx_pid_path: The path of nginx/passenger PID file. Default to /run/nginx.pid
prometheus_passenger_port: The port in which the exporter will expose the metrics. Default to 9149
prometheus_passenger_registry_dir: The location of `passenger_instance_registry_dir` setup in passenger configuration file. Default to /tmp
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - role: jobscore.prometheus_passenger_exporter
          prometheus_passenger_nginx_pid_path: /tmp/nginx.pid
          prometheus_passenger_port: 9999
          prometheus_passenger_registry_dir: /var/run/passenger

License
-------

[MIT](/LICENSE)

Author Information
------------------

This role was created by [GlauberrBatista](https://github.com/GlauberrBatista) while working for [JobScore Inc](https://jobscore.com).
