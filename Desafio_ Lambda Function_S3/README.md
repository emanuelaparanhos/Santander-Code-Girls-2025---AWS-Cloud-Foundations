# Desafio AWS Lambda Function e S3 - Bootcamp Santander Code Girls 2025
Este laboratório tem como objetivo de consolidar seus conhecimentos em tarefas automatizadas com Lambda Function e S3. O entregável é um repositório organizado contendo anotações e insights adquiridos durante a prática, servindo como material de apoio para os seus estudos e futuras implementações.

#CodeGirls2025 #WomenInTech

## Implementando Tarefas Automatizadas com Lambda Function e S3

###Passo 1 - Acesse CloudFormation na AWS
![CloudFormation](01-Acesse_CloudFormation.png)

###Passo 2 - Acesse a opção na aba lateral esquerda "Pilhas" e clique em "Criar pilha". Siga de acordo com as figuras abaixo. O nome será "desafioCloudFormationAutomatizada". Faça o upload do arquivo "automatizada.yaml" (lembre-se de alterar o nome do bucket para um nome único, sem maiúsculas e _).
![CriarPilha](01a-Criar_Pilha.png)
![CriarPilha2](02-Criar_Pilha.png)
![CriarPilha2](02a-Criar_Pilha.png)
![CriarPilha2](02b-Criar_Pilha.png)


###Passo 3 - Visualize a Pilha recém criada e vá a aba Eventos: Monitore CREATE_IN_PROGRESS para S3/IAM (condicional ativa). Tempo: 3-5 min 
![VisualizarPilha](03-Visualizar_Pilha.png)

###Passo 4 - Obeserve as saídas geradas. Verifique S3 e IAM Role
![Saida](04-Saida.png)
![VisualizarBucket](04-Visualizar_Bucket.png)
![VisualizarIAM](04-Visualizar_IAM.png)


Outputs e Teste: Acesse BucketURL; Teste role assume via AWS CLI (opcional). Upload no S3 para validar 
Update e Deleção: Para automação, atualize parâmetro (ex.: Ambiente para "prod") – veja diff nos eventos. Delete stack para cleanup.

