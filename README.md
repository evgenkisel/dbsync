# dbsync 

## Pre-steps

### Clone the project and open the file `db-push.yaml` to set the variables
```yaml
...
db_host:
db_user:
db_password:
db_name:
...
```

## How to PUSH

You need to run the command in the project's folder

```bash
ansible-playbook \
  --private-key <path_to_your_ssh_private_key> \
  -u <your_ssh_user> \
  -e local_dump_path=</absolut/path/to/file> \
  db-push.yaml
```