# Desafio AWS CloudFormation - Bootcamp Santander Code Girls 2025

```
Olá! Bem-vindo(a) ao meu repositório do desafio prático de AWS CloudFormation do Bootcamp Santander Code Girls 2025.
#CodeGirls2025 #WomenInTech
```


## Introdução à AWS e Conceitos Básicos
**Amazon S3** (Amazon Simple Storage Service) - é um serviços de armazenamento de objetos em nuvem oferecidos pela AWS. É ideal para armazenar, organizar e recuperar grandes volumes de dados de forma segura e escalável. Armazenamento de objetos na nuvem.\
**Amazon EC2** (Amazon Elastic Compute Cloud) - é um serviço da Amazon que fornece capacidade de computação escalável na nuvem do Amazon Web Services (AWS) através de máquinas virtuais, conhecidas como instâncias. Serviço de máquinas virtuais sob demanda.\
**Amazon EBS** (Elastic Block Store) - é um serviço para fornecer armazenamento em bloco fiável (também conhecido como volumes ou discos rígidos). Foi concebido para ser utilizado com instâncias do Amazon Elastic Compute Cloud (EC2).\
**Amazon Lambda Function** - Serverless é um novo paradigma onde os desenvolvedores não precisam gerenciar servidores. Este conceito nos ajuda a se preocupar somente com nosso código, não precisando gerenciar instâncias. Executa código sem gerenciar servidores.\
**Amazon AMI** (Amazon Machine Image) - é uma imagem de máquina virtual pré-configurada, que inclui as informações necessárias para iniciar uma instância, como o sistema operativo, o servidor de aplicações e as aplicações. Modelo de instância EC2 pré-configurado.\
***Amazon RDS*** (Amazon Relational Database Service) - é um serviço de banco de dados relacional de fácil gerenciamento.\
**Amazon Glacier** - é um dos tipos de armazenamento do Amazon S3. Ele oferece armazenamento durável para qualquer tipo de formato de dados que será acessado depois de 5 dias. O objetivo é pagar menos, arquivamento de longo prazo com baixo custo.\
**Amazon S3 Versioning** - ontrole de versões de objetos no S3.
**Amazon CDN** (Amazon CloudFront) - CDN para entrega rápida de conteúdo


Prepare o Template:

No Console CloudFormation > "Create stack" > "With new resources" > "Upload a template file".
Selecione minha-primeira-stack.yaml > Valide (deve mostrar "Template válido").
Especifique Detalhes:

Nome da stack: minha-primeira-stack-bootcamp.
Parâmetros: BucketName (ex.: bucket-seunome-2025-unico123), RoleName (default).
Adicione tag: Projeto: BootcampSantander2025.
Opções e Revisar:

Deixe padrão (role IAM automática).
Revise: Confirme 2 recursos (S3 e IAM).
Clique "Create stack" > Monitore até "CREATE_COMPLETE" (~2-5 min).
Teste:

Vá para S3 Console > Buckets > Upload arquivo no seu bucket.
Verifique Outputs para URL/ARN.
Limpeza: Delete a stack para remover recursos (veja seção abaixo).

Capturas de Tela: Stack Básica
Documentei o processo com screenshots reais do meu deploy inicial.

Processo de Criação
Criação da Stack Upload do template YAML e configuração de parâmetros (nome da pilha e BucketName único).

Stack Completa e Recursos
Stack Completa Status CREATE_COMPLETE na lista de stacks.

Recursos Criados S3 Bucket e IAM Role provisionados.

Logs de Criação (Eventos da Stack): Logs de Criação Histórico de eventos: Início da stack, criação do S3 Bucket e IAM Role, final com CREATE_COMPLETE.

Outputs e Teste no S3
Outputs da Stack BucketURL e RoleARN expostos para integração futura.

Teste S3 Bucket Upload bem-sucedido de arquivo teste no bucket criado, validando funcionalidade.

Evolução: Projeto 2 - Infraestrutura Automatizada
Para o desafio avançado, evolui a stack básica para uma versão mais robusta na pasta dedicada projeto-automatizado/. Adicionei condições (ex.: criar S3 só se parâmetro "sim"), tags automáticas (dinâmicas via !Ref para dev/prod) e policies gerenciadas para segurança. Isso demonstra idempotência em updates e reutilização em pipelines CI/CD.

Template Principal: stack-automatizada-corrigida.yaml – YAML validado com arrays em policies e AllowedValues.
Conceitos Aplicados: Conditions (!Equals), tags para governança, outputs condicionais. Testei updates (ex.: mudar Ambiente sem recriar tudo).
Por Quê Evoluir? Simula cenários reais: Flexibilidade para ambientes (dev/prod) e redução de recursos desnecessários.
Veja a documentação completa:

README-automatizado.md: Passos detalhados e pré-requisitos.
insights-automatizados.md: Reflexões pessoais (ex.: como automação reduz bias em setups manuais).
Capturas de Tela: Stack Automatizada
Parâmetros Avançados Configuração de condições (CriarBucket: sim) e tags dinâmicas.

Eventos Automatizados Logs de CREATE e UPDATE (idempotência em tags).

Recursos e Tags Lista de recursos com tags automáticas (Projeto e Ambiente).

Outputs e Teste S3 Outputs condicionais + upload no bucket para validação.


