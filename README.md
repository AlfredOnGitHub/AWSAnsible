AWS using Ansible

What is F2?

F2 stands for "Foundamentals lvl 2".

An AWS provisioning Ansible role.
`ansible-playbook main.yml -e "status="

Required values for "status": create or delete.

What you need:
- AWS.
- An user into AWS with programmatic access.
- A "keycred" file. A file with your credentials and variables so Ansible can read it.
You can call it whatever you want, but remember to modify the "main.yml" file so Ansible can get everything.
