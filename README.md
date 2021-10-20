# Ansible Role: microk8s

![MIT](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/gepaplexx/ansible-role-microk8s/Main?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/gepaplexx/ansible-role-microk8s?style=flat-square)
![GitHub Release Date](https://img.shields.io/github/release-date/gepaplexx/ansible-role-microk8s?style=flat-square)
![Maintenance](https://img.shields.io/maintenance/yes/2022?style=flat-square)

Install and configure [microk8s](https://microk8s.io/) - the smallest, simplest, pure production K8s on debian based systems.

## Requirements

* Ansible >= 2.10
* Linux Distribution
    * Debian Family
        * Ubuntu
            * Focal (20.04)

## Usage

### Role Variables

Some variables available in this role are listed here.  The full set is
defined in `[defaults/main.yml](defaults/main.yml)`.
* `microk8s_plugins`: Enable/disable various plugins.
* `microk8s_enable_ha`: Enable/disable high-availability.
* `microk8s_group_ha`: Hostgroup whose members will form HA cluster.
* `microk8s_csr_template`: If defined, will cause a custom CSR to be used in
  generating certificates.

### Basic playbook

```yaml
- hosts: servers
  roles:
    - role: gepaplexx.microk8s
      vars:
        microk8s_plugins:
          istio: true
          ingress: true
```

## License

MIT

## Author Information

This role is maintained by [Clemens Kaserer](https://www.ckaserer.dev/).

Contributions by:

- [@BabisK](https://github.com/BabisK)
- [@ckaserer](https://github.com/ckaserer)
- [@Defilan](https://github.com/defilan)
- [@dleske](https://github.com/dleske)
- [@dyasny](https://github.com/dyasny)
- [@ericpardee](https://github.com/ericpardee)
- [@eshikhov](https://github.com/eshikhov)
- [@istvano](https://github.com/istvano)
- [@markmywords](https://github.com/markmywords)
- [@Turiok](https://github.com/turiok)
- [@vonDowntown](https://github.com/vonDowntown)
