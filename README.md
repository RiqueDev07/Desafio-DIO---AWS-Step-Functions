# Desafio DIO - AWS Step Functions

## 📖 Descrição

Este repositório foi desenvolvido como parte do desafio da DIO sobre **AWS Step Functions**. O objetivo foi consolidar os conhecimentos adquiridos durante as aulas e documentar os principais conceitos relacionados à criação e automação de fluxos de trabalho (workflows) na AWS.

---

## 🎯 Objetivos do Laboratório

* Compreender o funcionamento do AWS Step Functions;
* Criar workflows utilizando máquinas de estado (State Machines);
* Integrar diferentes serviços da AWS de forma orquestrada;
* Documentar o aprendizado utilizando GitHub e Markdown.

---

## ☁️ O que é o AWS Step Functions?

O AWS Step Functions é um serviço de orquestração da AWS que permite criar fluxos de trabalho distribuídos através de máquinas de estado (State Machines). Cada etapa do processo é representada por um estado, facilitando a integração entre serviços como:

* AWS Lambda
* Amazon SQS
* Amazon SNS
* Amazon DynamoDB
* Amazon ECS
* Amazon EventBridge

O serviço oferece monitoramento visual das execuções, tratamento de erros e mecanismos de repetição automática (Retry).

---

## 🔄 Estrutura Básica de um Workflow

1. Início da execução.
2. Recebimento dos dados de entrada.
3. Processamento por uma função Lambda.
4. Validação dos resultados.
5. Decisão através de um estado Choice.
6. Finalização do fluxo.

Exemplo simplificado:

```
Start
  ↓
Processar Dados
  ↓
Validar Resultado
  ↓
[Sucesso?]
 ↙       ↘
Sim       Não
 ↓         ↓
Fim    Tentar Novamente
```

---

## 📚 Conceitos Aprendidos

### State Machine

Representa todo o fluxo de execução.

### States

São as etapas individuais do workflow.

Principais tipos:

* Task
* Choice
* Wait
* Parallel
* Map
* Pass
* Succeed
* Fail

### Retry e Catch

Permitem implementar tratamento de erros e novas tentativas de execução automaticamente.

### Integração com AWS Lambda

As funções Lambda executam pequenas tarefas sem necessidade de gerenciar servidores, sendo amplamente utilizadas dentro dos Step Functions.

---

## 💡 Insights Obtidos

* O AWS Step Functions facilita bastante a criação de processos complexos.
* A representação visual ajuda na identificação de falhas.
* O tratamento de exceções com Retry e Catch torna os fluxos mais resilientes.
* A integração nativa com diversos serviços AWS reduz a necessidade de código adicional.

---

## 🛠️ Tecnologias Utilizadas

* AWS Step Functions
* AWS Lambda
* Amazon SQS
* Git
* GitHub
* Markdown

---

## 📂 Estrutura do Repositório

```
/
├── README.md
└── images/
    ├── workflow.png
    └── state-machine.png
```

---

## 🚀 Conclusão

Este laboratório permitiu compreender como o AWS Step Functions pode ser utilizado para automatizar processos, integrar serviços e construir arquiteturas orientadas a eventos de forma organizada e escalável.

Além do aprendizado técnico, o desafio reforçou a importância da documentação e do uso do GitHub como ferramenta de compartilhamento de conhecimento.
