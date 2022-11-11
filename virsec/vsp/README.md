# VIRSEC Ansible Collection - virsec.vsp


## Installation

To install the collection, use the `ansible-galaxy` command:

```shell
$ ansible-galaxy collection install virsec.vsp
```

## Example usage


$$$$$$$$$$$$$$$$$$$$$$$$$$$$

The following examples are for reference purposes.

## Variable
Virsec VSP installation require few variables to be defined in `vars` directory, 
those varaibles are mainly CMS, LFR, Kafka IP addresses, and Install command

Install command e.g. for linux
"./vsp_install_vm.sh -i {{ inventory_hostname }} -c {{ cms_ip }} -l {{ lfr_ip }} -s web -u -k {{ kafka_ip }} -P -r"

Make Sure to read documentation to know meaning each flag in above command.

```yaml
---
- hosts: all

  collections:
    - virsec.vsp

  include_role:
    name: Install_virsec_vsp
```

## License
See the license for more details
https://github.com/achinnapurkar/ansible_virsec_vsp/blob/main/LICENSE
