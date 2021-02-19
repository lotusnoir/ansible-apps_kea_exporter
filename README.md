# Ansible Role: ansible-apps_kea_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_kea_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_kea_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_kea_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_kea_exporter)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_kea_exporter?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_kea_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_kea_exporter.svg)](https://github.com/lotusnoir/ansible-apps_kea_exporter/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_kea_exporter&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_kea_exporter)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_kea_exporter&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_kea_exporter)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_kea_exporter&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_kea_exporter)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_kea_exporter&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_kea_exporter)

Deploy [kea_exporter](https://github.com/mweinelt/kea-exporter) to expose kea metrics to prometheus.

## Role variables

| Name                           | Default Value  | Description                        |
| ------------------------------ | -------------- | -----------------------------------|
| `kea_exporter_version`         | 1.9.1          | kea_exporter version |
| `kea_exporter_build_dir`       | /tmp           | temporary directory to uncompress package |
| `kea_exporter_install_dir`     | /usr/local/bin | directory to install binary |
| `kea_exporter_force_install`   | false          | force install variable |
| `kea_exporter_listen_addresst` | 0.0.0.0        | listen address |
| `kea_exporter_listen_port`     | 9125           | port to expose prometheus metrics |
| `kea_exporter_listen_sock`     | /tmp/kea-dhcp4-ctrl.sock | port of the kea service on the kea server |

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

## Prometheus rules

TODO

## Grafana dashboard

A sample dashboard is available here: [https://grafana.com/grafana/dashboards/13571](https://grafana.com/grafana/dashboards/13571)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
