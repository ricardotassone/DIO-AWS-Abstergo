# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

**Data:** 29 de Maio de 2026  
**Empresa:** Abstergo Industries  
**Responsável:** Ricardo Tassone

---

## Introdução

Este relatório apresenta o processo de implementação de ferramentas na empresa **Abstergo Industries**, realizado por **Ricardo Tassone**. O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar **diminuição de custos imediatos** e otimizar a infraestrutura de TI da empresa, que atua como hub de distribuição farmacêutica e se comunica com múltiplas empresas parceiras.

---

## Descrição do Projeto

O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:

---

### Etapa 1:

- **Nome da ferramenta:** Amazon RDS (Relational Database Service)
- **Foco da ferramenta:** Gerenciamento de Banco de Dados gerenciado na nuvem
- **Descrição de caso de uso:**

A Abstergo Industries, como hub de distribuição farmacêutica, lida diariamente com grandes volumes de dados: pedidos, notas fiscais, controle de estoque, integração com fornecedores e distribuidoras parceiras. Atualmente, manter servidores de banco de dados on-premise implica custos fixos elevados com hardware, licenciamento, manutenção preventiva e equipe especializada.

Com a migração para o **Amazon RDS**, a empresa passa a utilizar um banco de dados totalmente gerenciado pela AWS, eliminando a necessidade de gerenciar infraestrutura física. O serviço oferece backups automáticos, atualizações de segurança, alta disponibilidade com Multi-AZ e escalabilidade sob demanda — pagando apenas pelo que utilizar.

**Vantagens para a Abstergo Industries:**
- Eliminação de custos com servidores físicos de banco de dados e manutenção de hardware
- Redução de licenciamento por meio de engines open-source como PostgreSQL ou MySQL
- Alta disponibilidade garantida pela AWS com SLA de 99,95%, evitando perdas financeiras por downtime
- Integração facilitada com sistemas de parceiros via endpoints seguros
- Escalabilidade automática em períodos de alta demanda (ex.: fechamento de pedidos em lote)

---

### Etapa 2:

- **Nome da ferramenta:** Amazon EC2 com Auto Scaling + AWS Savings Plans
- **Foco da ferramenta:** Gerenciamento otimizado de máquinas virtuais com redução de custos computacionais
- **Descrição de caso de uso:**

Distribuidoras farmacêuticas possuem picos sazonais de processamento — como lotes de pedidos, integrações em tempo real com parceiros e geração de relatórios regulatórios. Manter servidores físicos dimensionados para o pico máximo resulta em recursos ociosos e custos desnecessários na maior parte do tempo.

Com o **Amazon EC2 combinado ao Auto Scaling**, a empresa provisiona instâncias virtuais automaticamente conforme a demanda, aumentando ou reduzindo a capacidade computacional em tempo real. Aliado ao **AWS Savings Plans**, é possível obter descontos de até **66%** nos custos de computação ao comprometer-se com um plano de uso consistente por 1 ou 3 anos.

**Vantagens para a Abstergo Industries:**
- Fim dos gastos com servidores físicos ociosos — paga-se apenas pela capacidade utilizada
- Auto Scaling garante desempenho em picos de demanda sem superprovisionamento fixo
- Savings Plans reduzem drasticamente o custo por hora de instâncias EC2 usadas continuamente
- Facilidade de replicar ambientes entre regiões AWS para atender parceiros em diferentes localidades
- Ambientes de desenvolvimento/homologação podem ser desligados automaticamente fora do horário comercial, gerando economia adicional

---

### Etapa 3:

- **Nome da ferramenta:** Amazon S3 (Simple Storage Service) + S3 Intelligent-Tiering
- **Foco da ferramenta:** Armazenamento inteligente e econômico de documentos, laudos e arquivos regulatórios
- **Descrição de caso de uso:**

Empresas do setor farmacêutico geram e devem reter por anos uma grande quantidade de documentos: laudos de qualidade, notas fiscais eletrônicas, registros de rastreabilidade de medicamentos (SNGPC/ANVISA), contratos com distribuidoras parceiras e relatórios de auditoria. Armazenar esses arquivos em servidores locais ou soluções legadas gera custos crescentes com armazenamento físico, backup e recuperação de desastres.

O **Amazon S3** oferece armazenamento de objetos altamente durável (99,999999999% de durabilidade) com custo significativamente menor que infraestrutura local. Com o recurso **S3 Intelligent-Tiering**, arquivos acessados raramente são movidos automaticamente para camadas de armazenamento mais baratas, sem impacto na disponibilidade dos dados.

**Vantagens para a Abstergo Industries:**
- Redução de custos de armazenamento em até 95% comparado a soluções on-premise para arquivos frios
- Conformidade regulatória facilitada: S3 suporta políticas de retenção e imutabilidade para atender exigências da ANVISA
- Compartilhamento seguro de documentos com parceiros via URLs assinadas ou AWS PrivateLink
- Integração nativa com outros serviços AWS (RDS, EC2, Lambda) para workflows automatizados de documentos
- Backup e recuperação de desastres nativos, eliminando custos com soluções de DR dedicadas

---

## Conclusão

A implementação das ferramentas **Amazon RDS**, **Amazon EC2 com Auto Scaling + Savings Plans** e **Amazon S3 com Intelligent-Tiering** na empresa **Abstergo Industries** tem como resultado esperado:

- **Redução significativa de custos operacionais** com infraestrutura física, licenciamento e manutenção
- **Maior agilidade e escalabilidade** para suportar o crescimento do volume de distribuições e parceiros
- **Conformidade e segurança** adequadas às exigências regulatórias do setor farmacêutico
- **Alta disponibilidade** dos sistemas críticos, evitando perdas financeiras por indisponibilidade

Essas ações aumentarão a eficiência e a produtividade da empresa, modernizando sua infraestrutura de TI com um modelo de pagamento baseado em consumo real. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias AWS — como **AWS Lambda** para automação de integrações com parceiros e **Amazon CloudWatch** para monitoramento proativo de custos — que possam melhorar ainda mais os processos da empresa.

---

**Assinatura do Responsável pelo Projeto:**

Ricardo Tassone
