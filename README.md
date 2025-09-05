🚀 Desafio Estância EC2 – DIO Bootcamp

Este projeto apresenta uma arquitetura em AWS Cloud para armazenamento, processamento e backup de dados, com foco em escalabilidade, automação e segurança.
O objetivo é demonstrar como os dados percorrem todo o ciclo dentro da nuvem, desde o login do usuário até o backup seguro.

📌 Diagrama da Arquitetura

🛠️ Fluxo do Processo

1️⃣ Usuário e Login
O usuário acessa o sistema, realiza o login e garante a autenticação e controle de acesso.
🔒 Segurança é a base para governança em cloud.

2️⃣ Transferência de Dados
Os dados são enviados para a nuvem através de protocolos seguros (HTTPS/AWS SDK/CLI).

3️⃣ Armazenamento Inicial (Amazon S3)

Ponto central de entrada dos dados.

Escalabilidade quase ilimitada.

Durabilidade de 99,999999999%.

Integração com outros serviços AWS.

4️⃣ Upload Automatizado (AWS Lambda)

Acionado automaticamente quando arquivos chegam no S3.

Executa código sob demanda (event-driven).

Encaminha dados para a instância de processamento.

5️⃣ Processamento (Amazon EC2)

EC2 recebe os dados para processamento.

Configuração com AMIs customizadas.

Escalabilidade via Auto Scaling Groups.

Flexibilidade para diferentes cargas de trabalho.

6️⃣ Armazenamento Pós-Processamento

Dados originais e processados ficam separados.

Facilita auditoria, análises e consultas futuras.

7️⃣ Backup e Recuperação

Backup automático dos dados e AMIs.

Resiliência contra falhas.

Suporte a Disaster Recovery.

🔐 Segurança na Arquitetura

A arquitetura foi desenhada com foco em camadas de segurança, seguindo boas práticas da AWS:

IAM (Identity and Access Management) → usuários e permissões com princípio de menor privilégio

Criptografia (KMS/S3 Encryption) → dados criptografados em repouso e em trânsito

Proteção de Instâncias → Security Groups e NACLs para controlar tráfego

Backup Seguro → imagens (AMIs) e snapshots armazenados em ambientes protegidos

Governança → monitoramento via CloudTrail e CloudWatch Logs para auditoria e alertas

✅ Benefícios da Arquitetura

✔️ Escalabilidade → cresce conforme a demanda
✔️ Automação → upload e processamento sem intervenção manual
✔️ Segurança Reforçada → autenticação, criptografia, IAM e monitoramento
✔️ Custo-Efetivo → paga apenas pelo uso dos recursos
✔️ Resiliência → dados sempre protegidos contra falhas

🔮 Expansões Futuras

Machine Learning (SageMaker) → treinar modelos com os dados processados

Data Lake → integração com Athena, Glue e Redshift

Monitoramento Avançado → CloudWatch + CloudTrail para observabilidade
