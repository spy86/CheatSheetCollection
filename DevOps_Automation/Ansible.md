### Playbooks
```shell
    ansible-playbook <YAML>                   # Run on all hosts defined
    ansible-playbook <YAML> -f 10             # Run 10 hosts parallel
    ansible-playbook <YAML> --verbose         # Verbose on successful tasks
    ansible-playbook <YAML> -C                # Test run
    ansible-playbook <YAML> -C -D             # Dry run
    ansible-playbook <YAML> -l <host>         # Run on single host
```
Run Infos
```shell
    ansible-playbook <YAML> --list-hosts
    ansible-playbook <YAML> --list-tasks
```
Syntax Check
```shell
    ansible-playbook --syntax-check <YAML>
```
### Remote Execution
```shell
    ansible all -m ping
```
Execute arbitrary commands
```shell
    ansible <hostgroup> -a <command>
    ansible all -a "ifconfig -a"
```
### Debugging

List facts and state of a host
```shell
    ansible <host> -m setup                            # All facts for one host
    ansible <host> -m setup -a 'filter=ansible_eth*'   # Only ansible fact for one host
    ansible all -m setup -a 'filter=facter_*'          # Only facter facts but for all hosts
```
Save facts to per-host files in /tmp/facts
```shell
    ansible all -m setup --tree /tmp/facts
```
