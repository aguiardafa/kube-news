# Conteirizando sua aplicação NodeJS - kube-news

Neste repositório apresento o resultado do encapsulamento de uma aplicação construída em NodeJS em um Container Docker. O arquivo de encapsulamento <b>Dockerfile</b> segue uma configuração básica, cujo o principal objetivo é demonstra a facilidade na configuração, distribuição e execução de uma aplicação encapsulada em containers.

Há diversos benefícios em encapsular uma aplicação em container, mas o principal é a <b>portabilidade</b>, já que o projeto pode ser executado em qualquer máquina que possua o [Docker](https://docs.docker.com/get-docker/) instalado, tornando a Aplicação independente de sistema operacional e/ou qualquer outra configuração/instalação.

### Jornada DevOps de Elite - Aula 02:

Este repositório é parte da atividade pártica da Aula 02 do Curso [Jornada DevOps de Elite](https://www.devopspro.com.br/jornada-de-elite), ocorrido de 17 a 23 de outubro de 2022, promovido pela [Kubedev.io](https://kubedev.io/).

## 🛒 Requisitos do Projeto:

Antes de começar, você vai precisar ter instalado em sua máquina os seguintes recursos:

- [Git](https://git-scm.com/);
- [Docker](https://docs.docker.com/get-docker/);
- [K3d](https://k3d.io/v5.4.6/); e
- [Kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/).

## 📀 Executando o Projeto:

Para testarmos a aplicação, temos que executar os 4 passos a seguir:

1. [Fazer download do Projeto](#download-github)
2. [Criar Cluster Kubernetes](#build-cluster)
3. [Executar Manifesto Kubernetes](#run-manifesto)
4. [Acessar a Aplicação](#acessando-app)

<a name="download-github"></a>

### 1. Fazer downloado do Projeto

- Baixe este Repositório, executando o comando Git:

```bash
git clone git@github.com:aguiardafa/kube-news.git
```

<a name="build-cluster"></a>

### 2. Criar Cluster Kubernetes

1. Execute o comando abaixo para criar o Cluster Kubernetes para implantação do projeto:

```bash
k3d cluster create meucluster -p "80:30000@loadbalancer"
```

<a name="run-manifesto"></a>

### 3. Executar Manifesto

1. Pelo terminal, aberto na raiz da pasta `k8s` do Repositório, execute o comando para executar o manifesto kubernetes:

```bash
kubectl apply -f deployment.yaml
```

2. Execute o comando para verificar se a criação dos pods foi bem sucedida:

```bash
kubectl get pods
```

<a name="acessando-app"></a>

### 4. Acessar a Aplicação NodeJS

1. Pelo navegador de sua preferência, acesse a url `http://localhost` para visualizar a Aplicação;
2. Se os passos anteriores foram executados corretamente, a resposta será semelhante a tela abaixo:
<p align="center"><img alt="Kube-news" id="foto1" title="#FotoProjeto" height="450px" src="https://raw.githubusercontent.com/aguiardafa/kube-news/main/.github/kube-news.png" /></p>

## 👨‍💻Autor

<a href="https://github.com/aguiardafa" style="text-decoration: none;">
<img style="border-radius: 50% !important;" src="https://avatars.githubusercontent.com/u/16319889?v=4" width="48px" height="48px" alt="Diego Aguiar"/>
<br />
<span> Feito por Diego Aguiar 👋 Entre em contato! </span> 
</a>
