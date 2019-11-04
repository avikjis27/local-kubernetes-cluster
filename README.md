# Setting up local Kubernetes cluster using vagrant and ansible


- I have followed [this](https://kubernetes.io/blog/2019/03/15/kubernetes-setup-using-ansible-and-vagrant/) blog to setup local kubernetes cluster. 
- I did some required changes to run in my MAC book. Not very sure if those are required for other's.
- Your local system is expected to be equipped with Vagrant, some Vagrant provider like Oracle Virtual Box and Ansible.
- To create local cluster go inside the checked out folder and run `vagrant up`.
- Once everything comes out successfully check the following 
	- Run `vagrant ssh k8s-master`
	- Run `kubectl get nodes`
 	- Expected :

	```
	vagrant@k8s-master:~$ kubectl get nodes
	NAME         STATUS     ROLES    AGE     VERSION
	k8s-master   Ready      master   8m52s   v1.16.2
	node-1       Ready      <none>   3m42s   v1.16.2
	node-2       Ready   	<none>   33s     v1.16.2
	``` 
