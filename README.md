# aws-infra-atividade

## Passo a Passo
Criei Security Groups:
  a. Security Group para EC2_IFF:
  - Libertei o acesso SSH (porta 22) apenas para o meu IP pessoal.
  - Libertei o acesso HTTP (porta 80) – ou uma porta customizada – para qualquer IP (0.0.0.0/0).
    
![image](https://github.com/user-attachments/assets/12716e21-ae8d-4a0e-9393-3ce7495f31df)

  b. Security Group para RDS_IFF:
  - Permiti conexões via PostgreSQL (porta 5432) apenas para o Security Group da EC2 que havia sido criado anteriormente.
![image](https://github.com/user-attachments/assets/4fda2935-4e72-4897-8ac4-96e803ff4efe)


Criei uma Instância EC2:
  a. Utilizei a AMI Amazon Linux.
  b. Associei o Security Group criado para a EC2_IFF.
  c. Gereiei ou utilizei um par de chaves existente (.pem) para acesso via SSH.

![image](https://github.com/user-attachments/assets/5e007704-050f-43c3-9724-01af10f89086)

Criei um Banco de Dados via RDS (PostgreSQL):
  a. Selecionei o motor PostgreSQL.
  b. Associei o Security Group criado para o RDS_IFF.
  c. Configurei as credenciais de acesso (usuário e senha).
  d. Defini o nome do banco inicial para database-iff.
  e. Anotei o endpoint do banco de dados gerado.

![image](https://github.com/user-attachments/assets/3b6fbc63-98de-43e8-9bcb-1bc5684d44a3)


## SSH e CONEXÃO SQL

Fiz a conexão com o EC2 via ssh no PowerShell e dentro do EC2 instalei o postgresql para fazer a conexão com banco de dados.

![image](https://github.com/user-attachments/assets/d316d702-078c-4c07-b89d-584763b05154)

![image](https://github.com/user-attachments/assets/038931c0-a354-4e45-8035-954aa5736e99)




