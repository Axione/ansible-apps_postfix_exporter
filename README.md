# Ansible Role: ansible-apps_postfix_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_postfix_exporter.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_postfix_exporter)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__postfix_exporter-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_postfix_exporter/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_postfix_exporter/tags)

Deploy [postfix_exporter](https://github.com/boynux/postfix-exporter) to expose postfix metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `postfix_exporter_version` | 0.3.0 | postfix_exporter version |
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

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
