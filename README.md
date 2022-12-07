# dbsync 

## Pre-steps

### Clone the project and open the file `db-push.yaml` to set the variables
```yaml
...
server_a:
server_b:  
db_host:
db_user:
db_password:
db_name:
...
```

Open the file `inventories/hosts` and update it like
```text
[server_a]
XXX.XXX.XXX.XXX -> SERVER A IP address
[server_b]
YYY.YYY.YYY.YY -> SERVER B IP address
```

## How to PUSH

You need to run the command in the project's folder

```bash
ansible-playbook \
  -i inventories/ \
  --private-key <path_to_your_ssh_private_key> \
  -u <your_ssh_user> \
  -e local_dump_path=</absolut/path/to/file> \
  db-push.yaml
```