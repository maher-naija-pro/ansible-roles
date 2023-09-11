Manage_disks
=========

- Create an xfs filesystem on /dev/sda and mount it on /data (if we have only one disk)
- Create / extend lvm partitions on top of existing disks, format on xfs filesystem and mount it on /data (if we have more than two disks)
- Create raid0 partitions on top of existing disks, format on xfs filesystem and mount it on /data (if we have more than two disks) --> no possible extension with raid0

Requirements
------------


Role Variables
--------------
| Var  | Default | Comment |
| ---      | ---      | ---      |
| lvm   | yes | create lvm partitions when we have more than 2 disks|
| raid  | no | if yes create raid0 partitions when we have more than 2 disks |



Example Playbook
----------------
To create lvm partitions on vm-test-PPRD

ansible-playbook playbooks/manage-disks.yml -l vm-test-PPRD

To create raid0 partitions on vm-test-PPRD

ansible-playbook playbooks/manage-disks.yml -l vm-test-PPRD -e raid="yes"


License
-------


Author Information
------------------
M'RABET Firas
