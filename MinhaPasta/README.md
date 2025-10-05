# Desafio AWS CloudFormation Automatizada - Bootcamp Santander Code Girls 2025
Este laboratório tem como objetivo implementar uma infraestrutura automatizada com AWS CloudFormation. O entregável é um repositório organizado contendo anotações e insights adquiridos durante a prática, servindo como material de apoio para os seus estudos e futuras implementações.

#CodeGirls2025 #WomenInTech

## Implementando Stack com AWS CloudFormation Automatizada

###Passo 1 - Acesse CloudFormation na AWS
![CloudFormation](01-Acesse_CloudFormation.png)

###Passo 2 - Acesse a opção na aba lateral esquerda "Pilhas" e clique em "Criar pilha". Siga de acordo com as figuras abaixo. O nome será "desafioCloudFormationAutomatizada". será feito o upload do arquivo "automatizada.yaml".
![CriarPilha](01a-Criar_Pilha.png)
![CriarPilha2](02-Criar_Pilha.png)
![CriarPilha2](02a-Criar_Pilha.png)
![CriarPilha2](02b-Criar_Pilha.png)


###Passo 3 - Visualize a Pilha recém criada e vá a aba Eventos: Monitore CREATE_IN_PROGRESS para S3/IAM (condicional ativa). Tempo: 3-5 min 
![VisualizarPilha](03-Visualizar_Pilha.png)

###Passo 4 - Verifique S3 e IAM Role
![VisualizarBucket](04-Visualizar_Bucket.png)
![VisualizarIAM](03-Visualizar_IAM.png)


Outputs e Teste: Acesse BucketURL; Teste role assume via AWS CLI (opcional). Upload no S3 para validar 
Update e Deleção: Para automação, atualize parâmetro (ex.: Ambiente para "prod") – veja diff nos eventos. Delete stack para cleanup.
