# Teste de DevOps - CI/CD e Deploy no Kubernetes

## Objetivo

O objetivo deste teste é avaliar a capacidade do candidato em configurar uma esteira de CI/CD para a aplicação [api-node](https://github.com/tiagohique/api-node). A esteira deve realizar o deploy automatizado em um cluster Kubernetes e configurar um Horizontal Pod Autoscaler (HPA) para escalabilidade dinâmica.

## Requisitos do Teste

1. **Configuração do CI/CD**:
   - Utilize uma ferramenta de CI/CD como GitHub Actions, GitLab CI, Jenkins, ArgoCD ou outra de sua escolha.
   - O pipeline deve ser acionado a cada push na branch `main`.
   - O pipeline deve:
     - Construir a imagem Docker da aplicação.
     - Publicar a imagem no Docker Hub ou em outro registro de imagens (ECR, GCR, ACR, etc.).
     - Implantar a aplicação em um cluster Kubernetes.

2. **Configuração do Kubernetes**:
   - Criar os manifests Kubernetes necessários:
     - **Deployment** com pelo menos 2 réplicas iniciais.
     - **Service** do tipo LoadBalancer ou NodePort para exposição da aplicação.
     - **ConfigMap/Secret** caso necessário para armazenar configurações.
     - **HPA (Horizontal Pod Autoscaler)** configurado para escalar de **2 até 10 pods**, baseado no consumo de CPU (métrica recomendada: 70% de uso da CPU por pod).

3. **Entrega do Teste**:
   - Criar um repositório no GitHub ou GitLab contendo:
     - Arquivos de configuração do CI/CD.
     - Manifests Kubernetes.
     - Um `README.md` explicando como configurar e rodar o pipeline.
   - O candidato pode utilizar um cluster Kubernetes local (Minikube, Kind) ou um cluster gerenciado (EKS, GKE, AKS, OKE, etc.).

## Avaliação

O candidato será avaliado nos seguintes pontos:
- Estrutura e organização do repositório.
- Clareza e eficiência na configuração do CI/CD.
- Boas práticas no uso do Kubernetes.
- Capacidade de automação e escalabilidade da aplicação.
- Documentação clara e bem escrita.

Boa sorte! 🚀
