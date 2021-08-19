# Setup the control machine to run Ansible scripts

Run the command in the terminal:
```bash
  ansible-playbook 01-setup-control-machine.yml --ask-become-pass (or -K)
```

# Tasks:

## 1. Install required packages:
  1. **SSH Pass**. It allows you to provide the ssh password without using the prompt. This will be necessary for the first settings when we don't have a SSH keypair yet.

## 2. Add the IP and URL of each host into the /etc/hosts file:
    192.168.0.11 truenas01.aprendendo.com.br truenas01

## 3. Add the fingerprint of each host into the ~/.ssh/known_hosts file:
    truenas01.aprendendo.com.br,truenas01,192.168.0.11 ecdsa-sha2-nistp256 ...

## 4. Add passwords into the Secret Manager (Keychain):
  1. *truenas-root-password*. The password that will be used to authenticate with the root account.
  1. *truenas-smtp-password*. The password that will be used to authenticate when sending email notifications.

# Created by: 

1. Luciano Sampaio.
