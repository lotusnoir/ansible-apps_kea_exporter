# Ansible Role: ansible-apps_kea_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_kea_exporter.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_kea_exporter)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__kea_exporter-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_kea_exporter/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_kea_exporter/tags)

Deploy [kea_exporter](https://github.com/boynux/kea-exporter) to expose kea metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `kea_exporter_version` | 1.9.1 | kea_exporter version |
| `kea_exporter_build_dir` | /tmp | temporary directory to uncompress package |
| `kea_exporter_install_dir` | /usr/local/bin | directory to install binary |
| `kea_exporter_force_install` | false | force install variable |
| `kea_exporter_listen_addresst` | 0.0.0.0 | listen address |
| `kea_exporter_listen_port` | 9125 | port to expose prometheus metrics |
| `kea_exporter_listen_sock` | /tmp/kea-dhcp4-ctrl.sock | port of the kea service on the kea server |

## Examples

	---
	- hosts: apps_kea_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_kea_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
