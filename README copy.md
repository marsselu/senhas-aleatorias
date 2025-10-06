# Giropops Senhas

[![OpenSSF Best Practices](https://www.bestpractices.dev/projects/9384/badge)](https://www.bestpractices.dev/projects/9384)[![Build da imagem de container Redis](https://github.com/Tech-Preta/LINUXtips-PICK/actions/workflows/redis-docker.yml/badge.svg?branch=main)](https://github.com/Tech-Preta/LINUXtips-PICK/actions/workflows/redis-docker.yml) [![Build da imagem de container giropops-senhas](https://github.com/Tech-Preta/LINUXtips-PICK/actions/workflows/giropops-docker.yml/badge.svg)](https://github.com/Tech-Preta/LINUXtips-PICK/actions/workflows/giropops-docker.yml) [![Build e Distribuição de Pacotes com Melange e APKO](https://github.com/Tech-Preta/LINUXtips-PICK/actions/workflows/chainguard.yml/badge.svg)](https://github.com/Tech-Preta/LINUXtips-PICK/actions/workflows/chainguard.yml) [![CodeQL](https://github.com/Tech-Preta/giropops-senhas/actions/workflows/github-code-scanning/codeql/badge.svg)](https://github.com/Tech-Preta/giropops-senhas/actions/workflows/github-code-scanning/codeql) [![Dependabot Updates](https://github.com/Tech-Preta/giropops-senhas/actions/workflows/dependabot/dependabot-updates/badge.svg)](https://github.com/Tech-Preta/giropops-senhas/actions/workflows/dependabot/dependabot-updates) [![Image digest update](https://github.com/Tech-Preta/giropops-senhas/actions/workflows/digestabot.yml/badge.svg)](https://github.com/Tech-Preta/giropops-senhas/actions/workflows/digestabot.yml)

O projeto **Giropops Senhas** é uma aplicação web desenvolvida com Flask que permite a geração e gerenciamento de senhas. A aplicação utiliza Redis para armazenamento de dados e é containerizada usando Docker. Além disso, o projeto inclui integração contínua com GitHub Actions para construção e envio de imagens Docker, bem como verificação de vulnerabilidades.


# **NOTA IMPORTANTE**

Este projeto é baseado no **Giropops Senhas** e em vários momentos também se refere ao repositório desenvolvido pela ***[github.com/nataliagranato](https://)***. 

```mermaid
sequenceDiagram
    participant User
    participant WebApp
    participant Redis
    participant Prometheus
    participant Grafana

    User->>WebApp: Solicita geração de senha
    WebApp->>Redis: Armazena senha gerada
    WebApp->>User: Retorna senha gerada
    WebApp->>Prometheus: Exposição de métricas
    Prometheus->>Grafana: Coleta de métricas
    Grafana->>User: Exibe painel de monitoramento
```

# Links do Projeto

## Públicos

- **Aplicação pode ser acessada localmente em**: [https://senhas.nataliagranato.xyz](https://senhas.nataliagranato.xyz). Caso tenha problemas com o certificado, use a aba anônima.
- **Documentação do Projeto**: [https://devops.nataliagranato.xyz](https://devops.nataliagranato.xyz)
- **Pipelines**: [https://github.com/nataliagranato/LINUXtips-PICK/tree/develop/.github/workflows](https://github.com/nataliagranato/LINUXtips-PICK/tree/develop/.github/workflows)
- **Fórum de Discussão para Dúvidas**: [https://github.com/nataliagranato/LINUXtips-PICK/discussions](https://github.com/nataliagranato/LINUXtips-PICK/discussions)
- **Prometheus**: [https://prom.nataliagranato.xyz/](https://prom.nataliagranato.xyz/)
- **Grafana**: [https://grafana.nataliagranato.xyz/public-dashboards/56431da54e9143438ef8e5da78258347](https://grafana.nataliagranato.xyz/public-dashboards/56431da54e9143438ef8e5da78258347)
- **Pacotes**: [https://github.com/nataliagranato?tab=packages&repo_name=LINUXtips-PICK](https://github.com/nataliagranato?tab=packages&repo_name=LINUXtips-PICK)

## Privados

- **Helm Chart**: [https://github.com/nataliagranato/senhas](https://github.com/nataliagranato/senhas)
- **Registry**: `nataliagranato/senhas:1.0.0-amd64`

## Ferramentas e Tecnologias Utilizadas

![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white) ![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white) ![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![YAML](https://img.shields.io/badge/yaml-%23ffffff.svg?style=for-the-badge&logo=yaml&logoColor=151515) ![AquaSec](https://img.shields.io/badge/aqua-%231904DA.svg?style=for-the-badge&logo=aqua&logoColor=#0018A8) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white) ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white)

## Ferramentas e Tecnologias Utilizadas

- **Python**: Linguagem de programação principal.
- **Flask**: Framework web utilizado para construir a aplicação.
- **Redis**: Banco de dados em memória utilizado para armazenamento de dados.
- **Docker**: Utilizado para containerização da aplicação.
- **GitHub Actions**: Utilizado para integração contínua e automação de tarefas.
- **Cosign**: Utilizado para assinatura e verificação de imagens de contêiner.
- **Kyverno**: Utilizado para políticas de segurança no Kubernetes.
- **Kubernetes**: Utilizado para orquestração de contêineres em produção.
- **Prometheus**: Utilizado para monitoramento e alertas.
- **APKO**: Utilizado para construção de imagens de contêiner.
- **Melange**: Utilizado para construção de pacotes.
- **Helm**: Utilizado para gerenciamento de pacotes Kubernetes.
- **Hadolint**: Utilizado para verificação de qualidade de Dockerfiles.
- **Docker Scout**: Utilizado para verificação de vulnerabilidades em imagens de contêiner.
- **Snyk**: Utilizado para verificação de vulnerabilidades em dependências de aplicativos.
- **Trivy**: Utilizado para verificação de vulnerabilidades em imagens de contêiner.
- **CodeRabbit**: Utilizado para revisão de código.
- **DependaBot**: Utilizado para manter as dependências atualizadas.
- **Popeye**: Utilizado para verificação de configurações de cluster Kubernetes.
- **Grafana**: Utilizado para visualização de métricas.

## Utilizando em um cluster de desenvolvimento

1. Clone o repositório:

```bash
ansible-playbook atualizar_etc_hosts.yml
ansible-playbook deploy.yml
```

## Utilizando a aplicação localmente

1. Clone o repositório:

```bash
git clone https://github.com/Tech-Preta/giropops-senhas.git
cd giropops-senhas
```

2. Utilize o Compose

```bash
docker-compose up -d
```

4. Acesse a aplicação em seu navegador:

```
http://localhost:5000
```

## Contribuindo

Contribuições são bem-vindas! Por favor, siga as diretrizes abaixo ao contribuir para este projeto.

### Criando uma Issue

Se você encontrar um bug ou tiver uma ideia para uma nova funcionalidade, por favor, crie uma issue usando o template apropriado:

1. Vá para a aba "Issues" do repositório.
2. Clique em "New issue".
3. Selecione o template de bug ou feature request.
4. Preencha as informações necessárias e envie a issue.

### Fazendo um Pull Request

Para contribuir com código, siga os passos abaixo:

1. Fork o repositório.
2. Crie uma nova branch para sua feature ou correção de bug (`git checkout -b minha-feature`).
3. Faça as mudanças necessárias e adicione testes, se aplicável.
4. Commit suas mudanças (`git commit -m 'Adiciona minha nova feature'`).
5. Push para a branch (`git push origin minha-feature`).
6. Abra um pull request usando o template de pull request.

### Templates

- [Template de Pull Request](.github/PULL_REQUEST_TEMPLATE.md)
- [Template de Issue de Bug](.github/ISSUE_TEMPLATE/bug_report.md)