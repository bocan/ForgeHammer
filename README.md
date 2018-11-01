# ForgeHammer
Just a little Vagrant / Ansible project to give me a repeatable single-node Kubernetes cluster

## Info
This is a work in progress.  I'm basing it off [this excellent article](https://medium.com/@lizrice/kubernetes-in-vagrant-with-kubeadm-21979ded6c63) by Liz Rice, but augmenting and automating it with the Ansible side of [Kubespray](https://github.com/kubernetes-incubator/kubespray) from [The Kubernetes Incubator](https://github.com/kubernetes-incubator).  As the Ansible in question doesn't need to build a multi-node cluster, nor will ever run on anything other than Ubuntu and MAYBE RHEL, I'm cutting Kubespray **way** down and removing a huge amount of cruft.

I'm documenting this all as [an article here](https://medium.com/@bocan/a-vagrant-based-kubernetes-lab-29312b181e93) - it's still a draft so feel free to comment.
