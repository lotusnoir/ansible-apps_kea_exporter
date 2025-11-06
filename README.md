# ansible-apps_kea_exporter

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_kea_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_kea_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_kea_exporter.svg)](https://github.com/lotusnoir/ansible-apps_kea_exporter/releases/latest)
[![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_kea_exporter?color=orange&style=flat)](https://galaxy.ansible.com/lotusnoir/apps_kea_exporter)
[![downloads](https://img.shields.io/ansible/role/d/52261)](https://galaxy.ansible.com/lotusnoir/apps_kea_exporter)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/52261)](https://galaxy.ansible.com/lotusnoir/apps_kea_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Description](#description)
- [Requirements](#requirements)
- [Role variables](#role-variables)
- [Examples](#examples)
- [License](#license)
- [Author Information](#author-information)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Description

Deploy [kea_exporter]() to expose kea dhcp server metrics

## Requirements

none

## Role variables

See [variables](/defaults/main.yml) for more details.

## Examples

        ---
        - hosts: apps_kea_exporter
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-apps_kea_exporter

## Grafana Dashboard

You can find a grafana dashboard [here](https://grafana.com/grafana/dashboards/13925)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

## Author Information

- [Philippe LEAL](https://github.com/lotusnoir)
