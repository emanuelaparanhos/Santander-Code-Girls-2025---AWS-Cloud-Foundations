# Desafio AWS Lambda Function e S3 - Bootcamp Santander Code Girls 2025
Este laboratório tem como objetivo de consolidar seus conhecimentos em tarefas automatizadas com Lambda Function e S3. O entregável é um repositório organizado contendo anotações e insights adquiridos durante a prática, servindo como material de apoio para os seus estudos e futuras implementações.

#CodeGirls2025 #WomenInTech

## Implementando Tarefas Automatizadas com Lambda Function e S3

###Passo 1 - Crie um Bucket S3 na AWS ou tilizar um existente
![CriarS3](1-criar_S3.png)
![CriarS3](1-criar_S32.png)
![CriarS3](1-criar_S33.png)
![CriarS3](1-criar_S34.png)

###Passo 2 - Crie uma função IAM na AWS
![CriarRole](2-criar_role.png)
![CriarRole](2-criar_role2.png)
![CriarRole](2-criar_role3.png)
![CriarRole](2-criar_role4.png)
![CriarRole](2-criar_role5.png)

###Passo 3 - Criar um Lambda Function
![VisualizarPilha](03-Visualizar_Pilha.png)

###Passo 4 - Configurar Trigger
![Saida](04-Saida.png)
![VisualizarBucket](04-Visualizar_Bucket.png)
![VisualizarIAM](04-Visualizar_IAM.png)


Outputs e Teste: Acesse BucketURL; Teste role assume via AWS CLI (opcional). Upload no S3 para validar 
Update e Deleção: Para automação, atualize parâmetro (ex.: Ambiente para "prod") – veja diff nos eventos. Delete stack para cleanup.

