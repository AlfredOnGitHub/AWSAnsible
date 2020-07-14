AWS using Ansible

What is F2?
F2 stands for "Foundamentals lvl 2".

F2 connects with your localhost and import variables from a file called "keycred". It also have this "ansible_python_interpreter" variable due to a warning with fedora31 and ansible, so we need to specify the python version.

You can try to comment that line and run the playbook to see the warning.

Once it gets all the variables, it connects with AWS and do whatever you need.

Right now, it just can create and delete an instance, and create a keypair (linked with your publicid or whatever you want to put in).

Things that you need to run this playbook:

- AWS.
- An user into AWS with programmatic access.
- A "keycred" file. A file with your credentials and variables so Ansible can read it.
You can call it whatever you want, but remember to modify the "main.yml" file so Ansible can get everything.
