TechStock – Sistema de Controle de Estoque
📌 Sobre o Projeto
O TechStock é uma aplicação web para gerenciamento de estoque desenvolvida e implantada pela AlphaNexus Cloud utilizando serviços da AWS.

O sistema permite o controle de produtos, movimentações de estoque, alertas de reposição e monitoramento da infraestrutura em nuvem.

🏗 Arquitetura da Solução
A aplicação foi construída utilizando uma arquitetura em camadas:

Usuário
   │
   ▼
Application Load Balancer (ALB)
   │
   ├── Frontend (HTML, CSS e JavaScript)
   │
   └── Backend (Node.js)
            │
            ▼
      Amazon RDS
      PostgreSQL
Além disso, o ambiente conta com:

Prometheus para coleta de métricas

Grafana para visualização e monitoramento

Security Groups para controle de acesso

IAM para gerenciamento de permissões

☁️ Serviços AWS Utilizados
Serviço	Finalidade
EC2	Hospedagem da API Backend
RDS PostgreSQL	Banco de dados
Application Load Balancer	Balanceamento e roteamento
IAM	Controle de acesso
Security Groups	Segurança da rede
CloudWatch	Logs e monitoramento
Grafana	Dashboards
Prometheus	Métricas
🚀 Funcionalidades
Produtos
Cadastro de produtos

Edição de produtos

Exclusão de produtos

Consulta de estoque

Movimentações
Entrada de estoque

Saída de estoque

Ajuste de inventário

Histórico de movimentações

Alertas
Identificação automática de estoque mínimo

Exibição de produtos críticos

Dashboard
Total de produtos

Quantidade de alertas

Valor total em estoque

Movimentações recentes

🔀 Regras do Load Balancer
Prioridade	Caminho	Destino
1	/api*	Backend
2	/prometheus*	Prometheus
3	/grafana*	Grafana
4	/*	Frontend
🔒 Segurança
A infraestrutura foi configurada utilizando Security Groups específicos para:

Tráfego HTTP

Comunicação entre EC2 e RDS

Comunicação interna dos serviços

O banco de dados não possui acesso público direto, sendo acessado apenas pela aplicação.

📊 Monitoramento
Grafana
Responsável pela visualização de métricas e dashboards.

Prometheus
Responsável pela coleta e armazenamento das métricas da aplicação.

Métricas monitoradas:

Disponibilidade da aplicação

Consumo de recursos

Performance do backend

Saúde dos serviços

Testes Realizados
✅ Comunicação Frontend → Backend

✅ Comunicação Backend → RDS

✅ Consulta de produtos

✅ Balanceamento via ALB

AlphaNexus Cloud

Projeto desenvolvido para demonstrar a implantação completa de uma aplicação em ambiente AWS, utilizando boas práticas de infraestrutura, segurança, monitoramento e alta disponibilidade.

✅ Resultado
A solução foi implantada com sucesso, integrando Frontend, Backend, Banco de Dados, Balanceamento de Carga e Monitoramento em uma arquitetura totalmente hospedada na AWS.
