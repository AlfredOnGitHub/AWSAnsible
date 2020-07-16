AWS using Ansible

What is F2?
F2 stands for "Foundamentals lvl 2".

F2 connects with your localhost and import variables from a file called "keycred". It also have this "ansible_python_interpreter" variable due to a warning with fedora31 and ansible, so we need to specify the python version.

You can try to comment that line and run the playbook to see the warning.

Once it gets all the variables, it connects with AWS and do whatever you need.

What can you actually do with this?

Well, you can:

- Create and Terminate an specific instance.
- Terminate all running instances.
- Create a keypair using your own public ID.
- Get all the information of the instances, so you just need to filter it.
- Print all or specific info about your instances.

-- There is also a task called "wait 1 min". Why is that?
++ If you want to create an instance and then see all the running instances, you need to use the wait task. It is needed because when you create a new instance, it last a bit until it gets fully running, so you will not being able to see it until the whole proccess ends. That's why it is a minute, but you can do whatever you want with it.

Things that you need to run this playbook:

- AWS.
- An user into AWS with programmatic access.
- A "keycred" file. A file with your credentials and variables so Ansible can read it.
You can call it whatever you want, but remember to modify the "main.yml" file so Ansible can get everything.
