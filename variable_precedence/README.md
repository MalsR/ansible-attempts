By default ansible will use your default ssh to remote connect to machine in your inventory file. 
If an inventory file is not specified this will by default be under `/etc/ansible/hosts` file. 
Then run
`ansible all -m ping` #Will run ping on all the remote hosts listed 

http://docs.ansible.com/ansible/latest/intro_getting_started.html

To run a simple ansible command targeted to your machine. `-m` is telling ansible to use a module.
`ansible localhost -m ping`

Or you can use an ad-hoc ansible command
`ansible localhost -a "ls -la"`

```
malsr@Boeing777ER:~/workspace/ansible-attempts/variable_precedence$ ansible localhost -a "ls -la"
 [WARNING]: provided hosts list is empty, only localhost is available

localhost | SUCCESS | rc=0 >>
total 24
drwxrwxr-x 5 malsr malsr 4096 Aug  6 11:49 .
drwxrwxr-x 5 malsr malsr 4096 Aug  5 18:25 ..
drwxrwxr-x 2 malsr malsr 4096 Aug  5 18:21 group_vars
drwxrwxr-x 3 malsr malsr 4096 Aug  5 18:21 inventory
-rw-rw-r-- 1 malsr malsr    0 Aug  6 11:49 README.md
drwxrwxr-x 3 malsr malsr 4096 Aug  5 18:21 roles
-rw-rw-r-- 1 malsr malsr  319 Aug  5 18:21 show_variable_precedence.yaml
```
