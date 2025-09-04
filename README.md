# Desafio-Estancia-Ec2-Dio-Bootcamp

Este projeto apresenta um fluxo arquitetural desenvolvido em AWS Cloud, com foco em armazenamento, processamento e backup de dados.
A ideia é demonstrar como um usuário interage com o sistema desde o login até o processamento e a persistência dos dados, seguindo práticas de escalabilidade, automação e segurança.

Essa arquitetura reflete um ciclo completo de dados, englobando:

Entrada do usuário

Transferência e upload

Processamento automático

Armazenamento seguro

Backup para recuperação de desastres

🛠️ Fluxo do Processo
1️⃣ Usuário e Login

O processo inicia com a interação do usuário. Ele realiza login em uma aplicação cliente, que garante autenticação e controle de acesso.
👉 Esse passo é essencial para segurança e governança do ambiente.

2️⃣ Transferência de Dados

Após o login, os dados são enviados para a nuvem por meio de um processo de transferência segura, geralmente via protocolos HTTPS ou integração com AWS SDK/CLI.

3️⃣ Armazenamento Inicial (Amazon S3)

Os dados são armazenados no Amazon S3, que atua como ponto central de entrada.

Escalabilidade quase ilimitada

Alta durabilidade (99.999999999%)

Integração nativa com outros serviços AWS

4️⃣ Upload Automatizado (AWS Lambda)

Quando os arquivos chegam ao bucket S3, uma função Lambda é acionada automaticamente.

Gatilho event-driven

Executa código sob demanda

Encaminha os dados para a instância de processamento

Esse modelo elimina a necessidade de servidores dedicados para orquestração.

5️⃣ Processamento de Dados (Amazon EC2)

Uma instância de Amazon EC2 recebe os dados e realiza o processamento necessário.

Pode ser configurada com imagens customizadas (AMIs)

Permite escalabilidade horizontal (Auto Scaling Groups)

Oferece flexibilidade para cargas de trabalho diversas

6️⃣ Armazenamento Pós-Processamento

Após o processamento, os resultados são novamente armazenados em repositórios dedicados na nuvem.

Mantém dados originais e processados separados

Facilita auditoria, análise e consultas futuras

7️⃣ Backup e Recuperação

Para garantir resiliência, o ambiente possui backup automático dos dados e da imagem da instância.

Reduz riscos em caso de falha

Garante alta disponibilidade

Suporta disaster recovery

🚀 Benefícios da Arquitetura

✔️ Escalabilidade → Cresce junto com a demanda
✔️ Automação → Upload e processamento automáticos
✔️ Segurança → Controle de acesso, autenticação e backups
✔️ Custo-Efetivo → Paga-se apenas pelo uso dos recursos
✔️ Resiliência → Dados sempre protegidos contra falhas

🔮 Aplicações Futuras

Essa arquitetura pode ser expandida para:

Machine Learning (SageMaker) → Treinar modelos com dados processados

Data Lake → Integração com Athena/Glue/Redshift

Monitoramento Avançado → Uso de CloudWatch + CloudTrail

👨‍💻 Sobre o Projeto

Este repositório tem como objetivo demonstrar boas práticas em arquitetura cloud com AWS.
Mais do que tecnologia, a proposta é mostrar como a nuvem pode ser usada para:

Organizar dados

Gerar insights

Garantir segurança e confiança

