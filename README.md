# HW5-510

## Order of steps to run the ansible playbook:

## Using baker, by spinning a vm on the localhost:

1. Go to the directory containing the baker script and the playbook files.
2. Run `baker bake`
3. Run `baker run roles`
4. Run `baker run install`

The app will be running at localhost:8080

## Without baker on some other host

Requirements: The host should have ansible installed.

1. Go to the directory containing the playbook scripts.
2. Update the inventory file to add the ip addresses of the machines.
2. Run `ansible-playbook roles.yml -i inventory`
3. Run `ansible-playbook main.yml -i inventory`

The app will be running on port 8080.


