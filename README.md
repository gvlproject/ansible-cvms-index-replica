# ansible-cvms-index-replica
Ansible playbook for creating a cvmfs replica.

This playbook is based on the galaxyproject's
[infrastructure-playbook](https://github.com/galaxyproject/infrastructure-playbook/tree/9ad75c96e7be125768960f0bdd62fb30f569512f/roles/cvmfs).

to run this playbook,

1. Launch a CentOS 7 instance
2. Attach a volume for storing the replica data

Finally, run the playbook with:

    $ ansible-playbook -i inventory/hosts playbook.yml --extra-vars cvmfs_srv_device=/dev/vdc

**NOTE**: /dev/vdc is the device name of the volume abive