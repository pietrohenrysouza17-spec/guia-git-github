# 02 - Conceitos fundamentais do Git

## Repositório

Um repositório Git é o local onde o projeto e seu histórico de versões são armazenados.

Quando um projeto é iniciado com `git init`, o Git cria uma estrutura de controle de versão dentro da pasta do projeto.

## Commit

Um commit registra uma alteração no histórico do projeto.

Ele permite identificar o estado do projeto naquele momento e fornece informações como autor, data e mensagem da alteração.

Uma boa prática é criar commits pequenos e relacionados a uma única alteração lógica.

Exemplo:

```bash
git add README.md
git commit -m "docs: atualiza README"
```

## Snapshot

Um commit representa um snapshot, ou seja, um registro do estado lógico do projeto em determinado momento.

Os snapshots permitem acompanhar a evolução do projeto ao longo do tempo.

## Staging Area

A Staging Area é a área de preparação das alterações que serão incluídas no próximo commit.

O comando `git add` coloca arquivos ou alterações na Staging Area.

O fluxo básico é:

```text
Working Directory
       ↓ git add
Staging Area
       ↓ git commit
Repository
```

## Working Directory

O Working Directory corresponde aos arquivos do projeto que estão sendo trabalhados no computador.

Quando um arquivo é alterado, a mudança inicialmente fica no Working Directory.

É possível verificar essas alterações com:

```bash
git status
```

## Branch

Uma branch é uma referência que permite desenvolver uma linha de trabalho independente.

Branches não são cópias de pastas. Elas apontam para commits e permitem que diferentes linhas de desenvolvimento existam no mesmo repositório.

Para criar e entrar em uma nova branch:

```bash
git switch -c feature/exemplo
```

## Main

A branch `main` normalmente representa a principal linha de desenvolvimento do projeto.

Novas funcionalidades ou alterações podem ser desenvolvidas em branches separadas e posteriormente integradas à `main`.

## HEAD

`HEAD` indica a posição atual do Git, normalmente apontando para a branch ou commit que está sendo utilizado.

Por exemplo:

```text
HEAD -> main
```

significa que o estado atual está associado à branch `main`.

Em algumas situações, o Git pode entrar em estado de detached HEAD, quando o `HEAD` aponta diretamente para um commit em vez de uma branch.

## Merge

O `merge` integra alterações de uma branch em outra.

Por exemplo:

```bash
git switch main
git merge feature/exemplo
```

Nesse caso, as alterações da `feature/exemplo` são integradas à `main`.

## Fast-forward

Um fast-forward acontece quando a branch de destino não possui novos commits desde a criação da branch que será integrada.

Nesse caso, o Git pode simplesmente avançar a referência da branch.

## Three-way merge

Um three-way merge pode ocorrer quando as duas linhas de desenvolvimento possuem commits diferentes.

Nesse caso, o Git utiliza como referência:

* o commit comum entre as branches;
* o estado atual da primeira branch;
* o estado atual da segunda branch.

Dependendo das alterações, o Git pode criar um commit de merge.

## Conflitos

Um conflito acontece quando o Git não consegue combinar automaticamente alterações feitas na mesma região de um arquivo.

Durante um conflito, podem aparecer marcadores como:

```text
<<<<<<< HEAD
alteração da branch atual
=======
alteração da outra branch
>>>>>>> outra-branch
```

Para resolver o conflito, é necessário escolher ou combinar corretamente as alterações, remover os marcadores e salvar o arquivo.

Depois:

```bash
git add arquivo.md
```

e o merge pode ser concluído.

Caso seja necessário cancelar o merge:

```bash
git merge --abort
```

## Merge x Rebase

O `merge` integra duas linhas de desenvolvimento e preserva a estrutura de ramificação do histórico.

O `rebase` reaplica commits sobre uma nova base, podendo deixar o histórico mais linear.

O rebase pode alterar os hashes dos commits. Por isso, deve ser utilizado com cuidado em branches compartilhadas.

## Git distribuído

O Git é um sistema de controle de versão distribuído.

Quando um repositório é clonado, o usuário possui uma cópia do histórico do projeto, permitindo real
