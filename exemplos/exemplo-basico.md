# Exemplo básico de Git e GitHub

## Objetivo

Este exemplo apresenta um fluxo básico de utilização do Git para registrar uma alteração em um projeto e enviá-la para um repositório remoto no GitHub.

## Situação

Imagine que um estudante iniciou um projeto chamado `meu-projeto` e deseja utilizar o Git para controlar suas alterações.

### 1. Criar o repositório

Dentro da pasta do projeto, o estudante pode executar:

```bash
git init
```

Esse comando cria um repositório Git local.

### 2. Verificar o estado do projeto

```bash
git status
```

O comando mostra quais arquivos foram modificados, quais estão preparados para commit e quais ainda não estão sendo acompanhados pelo Git.

### 3. Adicionar um arquivo à Staging Area

Depois de criar ou modificar um arquivo:

```bash
git add README.md
```

Nesse momento, a alteração é colocada na área de preparação.

### 4. Criar o commit

Depois de preparar a alteração:

```bash
git commit -m "docs: adiciona README do projeto"
```

O commit registra a alteração no histórico do repositório.

### 5. Criar uma branch

Para desenvolver uma alteração de forma isolada:

```bash
git switch -c feature/novo-conteudo
```

Agora o estudante está trabalhando na branch `feature/novo-conteudo`.

### 6. Enviar a branch para o GitHub

Depois de realizar as alterações e criar os commits:

```bash
git push -u origin feature/novo-conteudo
```

O comando envia os commits da branch local para o repositório remoto.

### 7. Criar um Pull Request

No GitHub, o estudante pode criar um Pull Request para propor a integração da branch:

```text
feature/novo-conteudo → main
```

O Pull Request permite revisar as alterações antes que elas sejam integradas à branch principal.

### 8. Integrar a alteração

Depois da revisão, a branch pode ser integrada à `main` por meio do merge.

O fluxo completo pode ser representado assim:

```text
Alteração
    ↓
git status
    ↓
git add
    ↓
git commit
    ↓
git push
    ↓
Pull Request
    ↓
Revisão
    ↓
Merge
    ↓
main
```

## Exemplo de histórico

Depois de realizar algumas alterações, o histórico pode ser consultado com:

```bash
git log --oneline
```

Um exemplo de saída:

```text
a1b2c3d docs: adiciona exemplo básico
e4f5g6h docs: atualiza README
i7j8k9l docs: cria estrutura inicial
```

Cada linha representa um commit e apresenta seu identificador e sua mensagem.

## Boas práticas

Durante o desenvolvimento, algumas práticas ajudam a manter o histórico organizado:

* Criar commits pequenos e coerentes;
* Utilizar mensagens de commit claras;
* Criar branches para alterações específicas;
* Revisar alterações antes do merge;
* Evitar colocar informações sensíveis no repositório;
* Utilizar Pull Requests para facilitar a revisão;
* Consultar o histórico quando for necessário entender alterações anteriores.

## Resumo

O exemplo demonstra o fluxo básico de trabalho com Git e GitHub:

**alterar → preparar → commitar → enviar → revisar → integrar**

Esse fluxo pode ser adaptado para diferentes projetos e equipes de desenvolvimento.
