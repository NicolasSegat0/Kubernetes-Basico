# Kubernetes-Basico

## O que é um container? 
Container é um software usado para isolar, virtualmente, recursos de uma máquina física com o objetivo de operar aplicações.

## O que é um container engine?
Responsável pela criação do comntainer, assim, servindo para administração e trazendo a ideia de produto. Além de não conversar com o kernel da máquina. 

## O que é um container runtime? 
Especializado na comunicação com o kernel e responsável por rodar os containers. Ou seja, comunicação com alto nível.

## Kubernetes é um ecossistema
Software feito para orquestrar os outros containers e garantir uma boa funcionalidade. Caso um pare, existe um segundo para continuar o serviço. 

## Control Plane X Workers 
- Control Plane = Parte administrativa do cluster.
- Workers = Parte de serviços.

## Quais os componentes do Control Plane do Kubernetes? 
- Etcd = Banco do Cluster.
- Kube API Server = Conversa com todo o Cluster. Centralização do Cluster.
- Kube Scheduler = Gerenciamento/Agendamento dos Containers, caso um deles pare o serviço.
- Kube Controller = Estado do CLuster.

## Quais os componentes dos workers do Kubernetes?
- Kubelete = Agente do Cluster. 
- Kube Proxy = Proxy.

## Portas de cada componente: 
- API Server -> 6443.
- Etcd -> 2379 - 2380.
- Scheduler -> 10251.
- Kubelet -> 10250.
- Controller -> 10252.
- Node Port -> 30000 - 32767.

## Kubectl.
É a interação principal da API com o todo o kubernetes.

Kind: Simular um CLuster Kubernetes. 

- kind create cluster 

- kind delete cluster

- kubectl run --image nginx --port 80 (nome do cluster) 

- kubectl get pods

- source /root/.bash_profile

## Criação para teste. 

- kubectl run --image nginx --port 80 giropops --dry-run=client

- kubectl run --image nginx --port 80 giropops --dry-run=client -o yaml

- kubectl run --image nginx --port 80 giropops --dry-run=client -o yaml > pod.yaml

- kubectl apply -f pod.yaml
