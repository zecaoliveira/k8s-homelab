# Homelab Kubernetes
## Sessão para reconhecimento

Esta parte eu dedico a todos os profissionais que dedicam seu tempo para compartilhar o que aprenderam em sua maioria disponibilizando de graça na Internet.

----------------------------------------------------------------------------------
### "Se eu vi mais longe foi por estar sobre os ombros de gigantes." Isaac Newton!
----------------------------------------------------------------------------------

Sites que estou usando para compilar o meu homelab:

- Deploy a Production Ready Kubernetes Cluster: https://kubespray.io/#/?id=deploy-a-production-ready-kubernetes-cluster
- https://austinsnerdythings.com/2022/04/25/deploying-a-kubernetes-cluster-within-proxmox-using-ansible/
- https://blog.marcolancini.it/2021/blog-kubernetes-lab-baremetal/
- https://medium.com/@ebrar/how-to-install-kubernetes-on-fedora-coreos-with-using-kubespray-9a6e3a853436
- https://dev.to/admantium/kubernetes-installation-tutorial-kubespray-46ek
- https://stackoverflow.com/questions/52941015/how-to-find-master-node-from-worker-node-in-kubernetes
- https://ioflood.com/blog/zip-linux-command/#:~:text=To%20create%20a%20zip%20file,the%20following%20command%3A%20zip%20myfile.
- https://kubespray.io/#/?id=supported-linux-distributions
- https://stackoverflow.com/questions/68860301/what-is-the-difference-between-master-node-and-control-plane-on-kubernetes
- https://wiki-datacenter.unifique.com.br/pt-br/publico/cloud/kubernetes/deploy-cluster-fedora-coreos
- https://cri-o.io/
- https://git.geco-it.net/GECO-IT-PUBLIC/fedora-coreos-proxmox


## Implantar um cluster Kubernetes local usando automação (IaC)

Olá a todos.

A ideia deste projeto é estudar como as coisas funcionam nos bastidores. A cultura DevOps revolucionou a forma como entregamos soluções de software. Orquestradores de containers como Docker Swarm, Podman e Kubernetes revolucionaram a forma como as soluções, oriundas das ideias das diversas áreas de negócio, são provisionadas e entregues em questão de segundos.

Eu mesmo, em meu laboratório de estudos, fiquei impressionado em como em 33 segundos 3 máquinas estavam prontas para serem usadas como cluster.

Este documento está em construção então se sentir falta de alguma coisa é porque ela ainda está por vir. 

### Etapas a serem percorridas

Primeiro: configurar o processo de automação da criação de máquinas virtuais no Proxmox usando cloud-init e terraform: 
- https://github.com/zecaoliveira/k8s-fcos-proxmox

> Referência:
> - By Austins (Nerdy Things) -> https://austinsnerdythings.com/2021/09/23/deploying-kubernetes-vms-in-proxmox-with-terraform/

Segundo: configurar o processo de automação da criação do cluster Kubernetes usando o kubespray, ansible e python3: 
- https://github.com/zecaoliveira/kubespray-pve-k8s

> Referência:
> - By Pradeep Kumar ->https://www.linuxtechi.com/install-kubernetes-using-kubespray/
> - By Ebrar Leblebici -> https://medium.com/@ebrar/how-to-install-kubernetes-on-fedora-coreos-with-using-kubespray-9a6e3a853436

Terceiro: Configurar um service LoadBalancer para o cluster K8S em Homelab: https://github.com/zecaoliveira/k8s-metallb-homelab 
