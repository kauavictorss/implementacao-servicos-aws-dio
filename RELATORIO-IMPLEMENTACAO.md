# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

- **Data**: 13/03/2026
- **Empresa**: Abstergo Industries
- **Responsável**: Kauã Victor Silva dos Santos

## Introdução

Este relatório apresenta o processo de implementação de ferramentas na empresa **Abstergo Industries**, realizado por **Kauã
Victor Silva dos Santos**. O objetivo do projeto foi **elencar 3 serviços AWS**, com a finalidade de realizar **diminuição de
custos imediatos**.

## Descrição do Projeto

O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir,
serão descritas as etapas do projeto:

### Etapa 1: Amazon EC2 Auto Scaling

- **Nome da ferramenta:** Amazon EC2 Auto Scaling
- **Foco da ferramenta:** Otimização de recursos computacionais e redução de custos com servidores
- **Descrição de caso de uso:** Implementação do Auto Scaling para ajustar automaticamente a capacidade de instâncias
  EC2 conforme a demanda. Durante horários de pico (horário comercial), o sistema escala para até 10 instâncias,
  enquanto em períodos de baixa demanda (madrugada e finais de semana), reduz para 2 instâncias mínimas. Isso resultou
  em uma redução de aproximadamente 60% nos custos com servidores, eliminando o desperdício de recursos ociosos e
  garantindo performance apenas quando necessário.

### Etapa 2: Amazon S3 Intelligent-Tiering

- **Nome da ferramenta:** Amazon S3 com Intelligent-Tiering
- **Foco da ferramenta:** Otimização de armazenamento e redução de custos com dados
- **Descrição de caso de uso:** Migração de 500TB de dados do armazenamento on-premise para Amazon S3 com a classe
  Intelligent-Tiering ativada. Esta classe move automaticamente os dados entre camadas de acesso (Frequent Access,
  Infrequent Access, Archive e Deep Archive) baseado nos padrões de uso. Dados acessados raramente são movidos para
  camadas mais econômicas automaticamente. A implementação incluiu políticas de lifecycle para arquivos antigos e
  resultou em economia de 45% nos custos de armazenamento em comparação com o sistema anterior.

### Etapa 3: AWS Lambda (Serverless Computing)

- **Nome da ferramenta:** AWS Lambda
- **Foco da ferramenta:** Substituição de servidores dedicados por computação serverless
- **Descrição de caso de uso:** Migração de 15 microserviços de processamento batch que rodavam em servidores EC2
  dedicados 24/7 para AWS Lambda. Estas funções processam relatórios noturnos, envio de emails, processamento de imagens
  e integrações com APIs externas. Como o Lambda cobra apenas pelo tempo de execução real (milissegundos), eliminamos o
  custo de manter servidores rodando ociosamente. A mudança reduziu em 70% os custos desta operação, além de eliminar a
  necessidade de gerenciamento de infraestrutura e patches de segurança.

## Conclusão

A implementação de ferramentas na empresa Abstergo Industries tem como esperado uma redução total de aproximadamente R$ 85.000,00 mensais em custos de infraestrutura (cerca de 55% de economia), além de melhorias significativas em escalabilidade, disponibilidade e segurança. O Auto Scaling garante performance sob demanda, o S3 Intelligent-Tiering otimiza automaticamente o armazenamento, e o AWS Lambda elimina desperdícios com servidores ociosos. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa, como a futura implementação de Amazon RDS com Reserved Instances e AWS CloudWatch para monitoramento avançado.

## Documentação Complementar Recomendada

Em um cenário real de implementação, os seguintes documentos complementariam este relatório:

- **Manual de configuração do Auto Scaling** - Documentação técnica com configurações de políticas de escalonamento, métricas de CloudWatch e alarmes
- **Planilha comparativa de custos** - Análise financeira detalhada comparando custos antes/depois da implementação (on-premise vs AWS)
- **Documentação das funções Lambda** - Especificação técnica das 15 funções serverless, incluindo triggers, variáveis de ambiente e permissões IAM
- **Política de Lifecycle do S3** - Arquivo JSON com as regras de transição automática entre classes de armazenamento
- **Relatórios de monitoramento CloudWatch** - Dashboards e métricas dos primeiros 30 dias de operação pós-implementação
- **Diagramas de arquitetura AWS** - Representação visual da infraestrutura implementada

> **Nota:** Este é um projeto acadêmico desenvolvido para o desafio da DIO. Os documentos listados acima representam as melhores práticas que deveriam acompanhar uma implementação real.

## Links Úteis

- [Documentação oficial AWS Auto Scaling](https://docs.aws.amazon.com/autoscaling/)
- [Documentação oficial Amazon S3 Intelligent-Tiering](https://aws.amazon.com/s3/storage-classes/intelligent-tiering/)
- [Documentação oficial AWS Lambda](https://docs.aws.amazon.com/lambda/)
- [Calculadora de preços AWS](https://calculator.aws/)

### Assinatura do Responsável pelo Projeto:

Kauã Victor Silva dos Santos
