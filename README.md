# Configurando uma Instância de Banco de Dados na Azure

Este repositório foi criado como parte de um desafio da **DIO (Digital Innovation One)** com o objetivo de documentar os principais conceitos, etapas e boas práticas relacionados à configuração de uma instância de banco de dados na **Microsoft Azure**.

O material funciona como um resumo de estudos e como referência para futuras implementações em ambiente de nuvem.

## Objetivo do desafio

O laboratório tem como foco praticar o processo de configuração de um banco de dados na Azure, reforçando conceitos como:

- criação e configuração de recursos na nuvem;
- escolha das principais opções de uma instância de banco de dados;
- configuração de acesso e conectividade;
- segurança e controle de acesso;
- gerenciamento de custos e recursos;
- documentação técnica utilizando GitHub e Markdown.

## Azure SQL

O **Azure SQL** é a família de serviços de banco de dados relacionais da Microsoft baseada no SQL Server e oferecida como serviço gerenciado na Azure.

Uma das opções disponíveis é a **Instância Gerenciada de SQL do Azure (Azure SQL Managed Instance)**, que oferece alta compatibilidade com o SQL Server tradicional ao mesmo tempo em que a Microsoft gerencia grande parte da infraestrutura.

Entre as responsabilidades que podem ser simplificadas pelo uso de um serviço gerenciado estão:

- manutenção da infraestrutura;
- atualizações;
- alta disponibilidade;
- backups;
- monitoramento;
- escalabilidade dos recursos.

## Etapas gerais de configuração

### 1. Acessar o Portal do Azure

A configuração pode ser iniciada pelo Portal do Azure.

No portal, é possível pesquisar pelos serviços de banco de dados disponíveis e iniciar a criação de uma nova instância.

### 2. Definir a assinatura e o grupo de recursos

Durante a criação do recurso, é necessário selecionar:

- **Assinatura:** define em qual assinatura da Azure o recurso será provisionado;
- **Grupo de Recursos:** agrupamento lógico utilizado para organizar e administrar recursos relacionados.

Utilizar grupos de recursos ajuda a manter ambientes e projetos organizados.

### 3. Definir os dados da instância

Nesta etapa são configuradas informações como:

- nome da instância;
- região;
- método de autenticação;
- usuário administrador;
- capacidade computacional;
- armazenamento.

A região deve ser escolhida considerando fatores como disponibilidade dos serviços, latência e custos.

### 4. Configurar computação e armazenamento

A quantidade de recursos deve ser definida de acordo com a necessidade da aplicação.

Entre os principais pontos estão:

- capacidade de processamento;
- quantidade de memória;
- espaço de armazenamento;
- camada de serviço.

Em ambientes de estudo, é importante selecionar apenas os recursos necessários para evitar gastos desnecessários.

## Rede e conectividade

A configuração de rede é uma etapa importante em bancos de dados na nuvem.

Dependendo do serviço utilizado, pode ser necessário configurar:

- rede virtual (VNet);
- sub-redes;
- regras de firewall;
- endereços IP permitidos;
- conectividade privada;
- portas e regras de segurança.

Uma boa prática é liberar somente os acessos realmente necessários.

## Segurança

Alguns cuidados importantes ao trabalhar com bancos de dados na Azure:

- utilizar senhas fortes;
- evitar exposição pública desnecessária;
- aplicar o princípio do menor privilégio;
- revisar regras de firewall;
- utilizar identidades e permissões adequadas;
- manter credenciais fora do código-fonte;
- monitorar acessos e alterações.

Credenciais, strings de conexão e outros segredos **não devem ser versionados no GitHub**.

## Custos

Recursos de nuvem podem gerar cobrança enquanto estiverem provisionados.

Antes de criar uma instância, é importante verificar:

- tipo de serviço;
- quantidade de processamento;
- armazenamento contratado;
- região escolhida;
- tempo durante o qual o recurso permanecerá ativo.

Em laboratórios e estudos, uma boa prática é revisar os recursos criados ao terminar a atividade e excluir aqueles que não serão mais utilizados.

## Boas práticas aprendidas

Durante o estudo deste laboratório, alguns pontos importantes são:

1. planejar os recursos antes de provisioná-los;
2. organizar serviços utilizando grupos de recursos;
3. avaliar segurança e rede antes de liberar acessos;
4. verificar custos antes da criação do recurso;
5. documentar configurações e decisões importantes;
6. nunca armazenar credenciais diretamente no repositório;
7. excluir recursos de laboratório quando eles não forem mais necessários.

## Fluxo resumido

```text
Portal do Azure
      ↓
Grupo de Recursos
      ↓
Serviço de Banco de Dados
      ↓
Configuração da Instância
      ↓
Computação e Armazenamento
      ↓
Rede e Segurança
      ↓
Revisão das Configurações
      ↓
Criação do Recurso
      ↓
Validação da Conectividade
```

## Conclusão

Este desafio permitiu revisar o processo de configuração de um banco de dados na Microsoft Azure e entender melhor os principais pontos que devem ser considerados ao utilizar um serviço de banco de dados em nuvem.

Além da criação do recurso, aspectos como **segurança, conectividade, organização, escalabilidade e custos** são fundamentais para uma implementação adequada.

A documentação do processo também é importante, pois facilita a manutenção do ambiente e cria uma base de conhecimento para projetos futuros.

## Referências

- [Documentação do Azure SQL](https://learn.microsoft.com/pt-br/azure/azure-sql/)
- [Início Rápido: criar uma Instância Gerenciada de SQL do Azure](https://learn.microsoft.com/pt-br/azure/azure-sql/managed-instance/instance-create-quickstart)
- [Documentação do GitHub](https://docs.github.com/)
- [Sintaxe Markdown no GitHub](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

---

**Desafio de Projeto — DIO**
