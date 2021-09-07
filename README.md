# Setup a TrueNAS HomeLab using Ansible

The playbook can setup one or more servers running TrueNAS Core 12.

Run the command in the terminal:
```bash
  ansible-playbook site.yml --ask-become-pass (or -K)
```

# Roles you can execute:
1. [Setup](roles/01-control-machine/README.md) the control machine to run Ansible scripts.
1. [Setup](roles/02-system/README.md) the system's preferences.
1. [Setup](roles/05-network/README.md) the network.
1. [Setup](roles/06-storage/README.md) the storage pools.
1. [Setup](roles/08-sharing/README.md) NFS and iSCSI sharing.
1. [Setup](roles/09-services/README.md) the services that will be used by TrueNAS.

# Variables:

1. debug

Specify if more messages should be displayed during the executions.
If no value is passed, the default value **false** will be used.

  ```json
  --extra-vars='{"debug":false}'
  ```

# Links:

[Links](links.md "Links")

# License:

[MIT](LICENSE "MIT License")

# Created by: 

1. Luciano Sampaio.
