# Virsec VSP installation

VSP Probe (Server which need to be protected), can be installed on Linux or Windows machines
There are 2 yml files for each

Note:
Define Few varaibles under vars Directory for Linux or windows, namely for CMS, KAFKA, LFR IP address, Along with Install command

Note:
VSP installation need ansible user to have root or sudo to root Privileges

Sample Inventory against which VSP roles can be used



[all:vars]
ansible_user=<Ansible Username>
ansible_ssh_common_args="-o StrictHostKeyChecking=no -o UserKnownHostsFile=/dev/null"
[all]
1.2.3.4
1.2.3.5
1.2.3.6



Sample Variable file for Linux based VSP probe installation
---
lfr_ip: 10.30.2.14
cms_ip: 10.30.2.14
kafka_ip: 10.30.2.14
install_var: "./vsp_install_vm.sh -i {{ inventory_hostname }} -c {{ cms_ip }} -l {{ lfr_ip }} -s web -u -k {{ kafka_ip }} -P -r"


## License
See the license for more details
https://github.com/achinnapurkar/ansible_virsec_vsp/blob/main/virsec/vsp/LICENSE
