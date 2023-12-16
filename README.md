# deploy-st2-on-rancher

```
vscode@XXXXXXXXXXXX:/workspace/ansible$ ansible-galaxy role install -r requirements.yml
vscode@XXXXXXXXXXXX:/workspace/ansible$ ansible-playbook -i inventories/dev/hosts.ini playbooks/site.yml --extra-vars=@extra_vars/common.yml
vscode@XXXXXXXXXXXX:/workspace/ansible$ ansible-playbook -i inventories/dev/hosts.ini playbooks/site.yml
```

```
kubectl -n kube-system edit configmaps canal-config
kubectl -n kube-system rollout restart daemonset canal
```
