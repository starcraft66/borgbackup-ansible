# borgbackup-ansible

## A simple ansible role/playbook to manage multiple clients backing up to a central borg repo server

---

## Setup

To use this playbook you must add your central repo server to the `repo_server` group and all of your clients to the `backup_client` group in tour inventory file. Additionally, every client must have its repo encryption key supplied via a `repo_encryption_key` host variable in the inventory. See the `inventory.example` file for an example.

Aditional configuration options may be changed in the `group_vars/all` yaml configuraiton file.

## Running

To run the playbook, simply call ansible-playbook like so:

    ansible-playbook -i inventory play.yml