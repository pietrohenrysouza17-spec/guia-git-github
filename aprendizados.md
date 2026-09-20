# Aprendizados do Projeto

## Introdução

Durante o desenvolvimento deste projeto, foram estudados e praticados os principais conceitos relacionados ao Git e ao GitHub.

A construção do guia permitiu aplicar os conceitos estudados em uma situação prática, utilizando branches, commits, Pull Requests e merges.

## Principais aprendizados

### Git e GitHub

Foi possível compreender que Git e GitHub são ferramentas relacionadas, mas possuem funções diferentes.

O Git é um sistema distribuído de controle de versão utilizado para registrar e acompanhar alterações em projetos.

O GitHub é uma plataforma que permite hospedar repositórios Git e facilita a colaboração entre desenvolvedores.

### Commits

Um dos principais aprendizados foi compreender a função dos commits.

O commit registra uma alteração no histórico do projeto, permitindo acompanhar a evolução dos arquivos.

Também foi possível perceber a importância de utilizar mensagens claras e realizar commits pequenos e coerentes.

### Staging Area

Foi aprendido que o `git add` não cria um commit.

Ele coloca as alterações na Staging Area, preparando-as para serem registradas pelo `git commit`.

O fluxo básico aprendido foi:

```text
Working Directory
       ↓
   git add
       ↓
Staging Area
       ↓
  git commit
       ↓
Repository
```

### Branches

As branches permitem desenvolver alterações de forma isolada sem modificar diretamente a linha principal do projeto.

Durante o projeto foram utilizadas branches diferentes para desenvolver módulos e exemplos.

Isso ajudou a compreender na prática como o trabalho pode ser dividido em funcionalidades ou partes do projeto.

### Pull Requests

Foi possível compreender o Pull Request como uma forma de propor alterações para integração em outra branch.

Durante o projeto foram criados Pull Requests para integrar diferentes partes do guia à `main`.

Esse processo também permitiu revisar as alterações antes da integração.

### Merge

O merge foi utilizado para integrar o conteúdo desenvolvido nas branches à `main`.

A utilização do histórico com `git log --graph` ajudou a visualizar como as branches foram criadas e posteriormente integradas.

### GitHub e colaboração

O projeto também permitiu praticar o envio de branches para um repositório remoto utilizando `git push`.

Foi possível perceber a diferença entre trabalhar localmente e enviar as alterações para o GitHub.

## Dificuldades encontradas

Uma das principais dificuldades foi compreender inicialmente a diferença entre os estados dos arquivos e as etapas necessárias para registrar uma alteração.

Também foi necessário entender que criar um commit local não significa que a alteração já está disponível no GitHub.

Outro ponto importante foi compreender que uma branch precisa ser integrada à `main` para que suas alterações façam parte da linha principal do projeto.

## Como as dificuldades foram resolvidas

As dificuldades foram resolvidas por meio da prática dos comandos e da consulta ao estado do repositório utilizando `git status`.

A utilização do `git log` também ajudou a verificar se os commits haviam sido registrados corretamente.

O uso de Pull Requests permitiu compreender melhor o processo de integração entre branches.

## Aplicação profissional

Os conhecimentos adquiridos podem ser utilizados em projetos acadêmicos e profissionais de desenvolvimento de software.

Git e GitHub permitem organizar o histórico do projeto, trabalhar com branches, revisar alterações e colaborar com outras pessoas.

Esses recursos são importantes para manter um fluxo de desenvolvimento organizado e facilitar o acompanhamento das mudanças realizadas no código.

## Conclusão
A prática contribuiu para compreender melhor o fluxo de versionamento.

A realização do projeto possibilitou transformar os conceitos estudados sobre Git e GitHub em uma experiência prática.

Além de aprender comandos individuais, foi possível compreender um fluxo completo de trabalho, desde a criação de alterações até sua revisão e integração na branch principal.

A prática contribuiu para desenvolver uma compreensão inicial do controle de versão e de sua importância no desenvolvimento de software.
