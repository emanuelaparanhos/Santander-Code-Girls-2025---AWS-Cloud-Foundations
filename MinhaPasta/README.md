Implementando Infraestrutura Automatizada com AWS CloudFormation
Este é o componente dedicado ao desafio "Implementando Infraestrutura Automatizada com AWS CloudFormation" no Bootcamp Santander Code Girls 2025. Aqui, evoluo a stack básica (do desafio pratico do módulo anterior) para uma versão mais robusta, com condições e tags automáticas. Foquei em documentar o processo para reutilização futura, aplicando conceitos como idempotência e parâmetros dinâmicos.

Conceitos Aplicados
Automatização Avançada: Condições (!Equals) para recursos opcionais; tags dinâmicas (!Ref) para ambientes (dev/prod).
Idempotência: Re-deploy sem recriar recursos – CloudFormation gerencia diffs.
Integração: Outputs para chaining com outras stacks (ex.: AWS CLI scripts).
Minha Experiência: Após as aulas, adicionei condições para simular cenários reais (ex.: bucket só em prod). Erro comum: Parâmetros inválidos – validei com AllowedValues.
Pré-Requisitos
Conta AWS Free Tier.
Template: stack-automatizada.yaml.
Ferramentas: Console AWS, GitHub para versionamento.
Passo a Passo da Implementação
Validação do Template: No CloudFormation Create Stack > Upload YAML > Verifique sintaxe e preview.
Configuração de Parâmetros: Nome stack: stack-automatizada; BucketName: único; CriarBucket: "sim"; Ambiente: "dev" 
Deploy e Monitoramento: Crie stack > Eventos: Monitore CREATE_IN_PROGRESS para S3/IAM (condicional ativa). Tempo: 3-5 min 
Recursos e Tags: Verifique S3 (se criado) com tags; IAM Role com policy 
Outputs e Teste: Acesse BucketURL; Teste role assume via AWS CLI (opcional). Upload no S3 para validar 
Update e Deleção: Para automação, atualize parâmetro (ex.: Ambiente para "prod") – veja diff nos eventos. Delete stack para cleanup.
