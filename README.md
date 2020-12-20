## STEP 1: Update the local & remote file path in playbook.yml
```
vars:
    src_remote_machine_file_path: "/home/ubuntu/test.txt"
    dest_local_machine_file_path: "/Users/foobar/ansible-download"
```

## STEP 2: Update host file
```
[my-servers]
	3.137.136.225 ansible_ssh_private_key_file=/Users/foobar/Downloads/foobar.pem ansible_ssh_user=ubuntu
  9.137.136.100 ansible_ssh_private_key_file=/Users/foobar/Downloads/foobar.pem ansible_ssh_user=ubuntu
```

## STEP 2: Run the playbook
```
ansible-playbook -i hosts playbook.yml
```