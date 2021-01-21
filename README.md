# Ansible Role: ansible-apps_postfix_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_postfix_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_postfix_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_postfix_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_postfix_exporter)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_postfix_exporter?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_postfix_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_postfix_exporter.svg)](https://github.com/lotusnoir/ansible-apps_postfix_exporter/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_postfix_exporter&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_postfix_exporter)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_postfix_exporter&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_postfix_exporter)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_postfix_exporter&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_postfix_exporter)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_postfix_exporter&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_postfix_exporter)

Deploy [postfix_exporter](https://github.com/boynux/postfix-exporter) to expose postfix metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `postfix_exporter_version` | 0.3.0 | postfix_exporter version |
| `postfix_exporter_install_dir` | /usr/local/bin | directory to install binary |
| `postfix_exporter_force_install` | false | force install variable |
| `postfix_exporter_logfile` | /var/log/mail.log | path to postfix logs |
| `postfix_exporter_listen_port` | 9124 | port to expose prometheus metrics |

## Examples

	---
	- hosts: apps_postfix_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_postfix_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
