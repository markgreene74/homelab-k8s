# homelab-k8s

Simple workflow to build to build a Kubernetes cluster using the `geerlingguy.kubernetes` role.

## preparation work

-  make sure Ansible can run on all the vms

```
ansible all -m ping
```

- install the `kubernetes` and `docker` roles under `roles/` using `ansible-galaxy`

```
ansible-galaxy install --roles-path ./roles geerlingguy.kubernetes
ansible-galaxy install --roles-path ./roles geerlingguy.docker
```

## run the playbook

- make sure to change the variables, check the hostfile `k8s-hosts`

- run the playbook

```
ansible-playbook main.yml
```


## links
- https://galaxy.ansible.com/geerlingguy/kubernetes
- https://galaxy.ansible.com/geerlingguy/docker
