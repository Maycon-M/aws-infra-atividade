# aws-infra-atividade

## passo a passo
Criei Security Groups:
  a. Security Group para EC2_IFF:
  - Libertei o acesso SSH (porta 22) apenas para o meu IP pessoal.
  - Libertei o acesso HTTP (porta 80) – ou uma porta customizada – para qualquer IP (0.0.0.0/0).
  b. Security Group para RDS_IFF:
  - Permiti conexões via PostgreSQL (porta 5432) apenas para o Security Group da EC2 que havia sido criado anteriormente.

Criei uma Instância EC2:
  a. Utilizei a AMI Amazon Linux.
  b. Associei o Security Group criado para a EC2_IFF.
  c. Gereiei ou utilizei um par de chaves existente (.pem) para acesso via SSH.

Criei um Banco de Dados via RDS.

Criei um Banco de Dados via RDS (PostgreSQL):
  a. Selecionei o motor PostgreSQL.
  b. Associei o Security Group criado para o RDS_IFF.
  c. Configurei as credenciais de acesso (usuário e senha).
  d. Defini o nome do banco inicial para database-iff.
  e. Anotei o endpoint do banco de dados gerado.

## SSH e CONEXÃO SQL

Fiz a conexão com o EC2 via ssh no PowerShell e dentro do EC2 instalei o postgresql para fazer a conexão com banco de dados.

