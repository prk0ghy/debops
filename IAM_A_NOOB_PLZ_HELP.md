### How to install from source:

### Method A:
#### setup python virutalenv

```bash
mkdir ~/src/venv/debops
virutalenv ~/src/venv/debops
```
#### enter the python virtualenv with

```bash
source ~/src/venv/debops/bin/activate
```

#### you can leave the python venc with

```bash
deactivate  
```
### Method B:
#### python in unix user environment:

```bash
git clone git@github.com:debops/debops.git ~/.local/share/debops/debops
cd ~/.local/share/debops/debops
sudo ./setup.py install
```


## debops-ng

Q: Why is there debops-ng?

@ikmaak:
wow, debops-ng? i am trying to find a page that describes the goals of that project. thanks in advance, and for the great work already done :)

@drybjed:

what I want to do with the new scripts is: switch to a Class-based model; switch from separate debops-* binaries to subcommands, focus on Ansible Collections as the default "container" for playbooks and roles, add proper support for git-crypt

currently most of things work - you can create new projects, run playbooks, etc. what is missing from feature parity with current scripts is support for encfs

so when that gets added, the new scripts will replace the old ones. what will change that instead of 'debops', you will have to use 'debops run' to execute any playbooks

and the 'site.yml' playbook will not be a default anymore, but you will be able to define a default playbook per inventory

when that's done, I want to work on implementing new project directories with multiple inventories, revamp PKI support to add CA bridge, add support for multiple inventory types (ansible-roster, netbox)

wow, debops-ng? i am trying to find a page that describes the goals of that project. thanks in advance, and for the great work already done :)


