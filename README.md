# deploy-st2-on-rancher

```
vscode@XXXXXXXXXXXX:/workspace/ansible$ ansible-galaxy role install -r requirements.yml
vscode@XXXXXXXXXXXX:/workspace/ansible$ ansible-playbook -i inventories/dev/hosts.ini playbooks/site.yml --extra-vars=@extra_vars/common.yml
vscode@XXXXXXXXXXXX:/workspace/ansible$ ansible-playbook -i inventories/dev/hosts.ini playbooks/site.yml
```

sudo docker run -d --privileged --restart=unless-stopped --net=host -v /etc/kubernetes:/etc/kubernetes -v /var/run:/var/run rancher/rancher-agent:v2.6.7 --server https://10.0.2.9:443 --token svx972ktnn4g94fsvp99nwq4z6hpsd8l4r97qqbvvg7d8qwkxgtpb2 --ca-checksum d247f0bcf343b4195411a522de82adebc3daeea88f9e34fea999a62dd63e93ef --etcd --controlplane

sudo docker run -d --privileged --restart=unless-stopped --net=host -v /etc/kubernetes:/etc/kubernetes -v /var/run:/var/run rancher/rancher-agent:v2.6.7 --server https://10.0.2.9:443 --token svx972ktnn4g94fsvp99nwq4z6hpsd8l4r97qqbvvg7d8qwkxgtpb2 --ca-checksum d247f0bcf343b4195411a522de82adebc3daeea88f9e34fea999a62dd63e93ef --worker

sudo docker run -d --privileged --restart=unless-stopped --net=host -v /etc/kubernetes:/etc/kubernetes -v /var/run:/var/run rancher/rancher-agent:v2.6.7 --server https://10.0.2.9:443 --token v8f92h5wlggjpnjxvnwqxts429wrdt6xx25cq5xjhkgk6gk6g75fx6 --ca-checksum d247f0bcf343b4195411a522de82adebc3daeea88f9e34fea999a62dd63e93ef --etcd --controlplane

sudo docker run -d --privileged --restart=unless-stopped --net=host -v /etc/kubernetes:/etc/kubernetes -v /var/run:/var/run rancher/rancher-agent:v2.6.7 --server https://10.0.2.9:443 --token v8f92h5wlggjpnjxvnwqxts429wrdt6xx25cq5xjhkgk6gk6g75fx6 --ca-checksum d247f0bcf343b4195411a522de82adebc3daeea88f9e34fea999a62dd63e93ef --worker
