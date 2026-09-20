# 03 - Exercícios práticos de Git e GitHub

## Objetivo

Este módulo apresenta exercícios práticos para fixar os principais conceitos e comandos estudados nos módulos anteriores.

As atividades foram organizadas de forma gradual, começando por comandos básicos e avançando para branches, commits e integração de alterações.

## Exercício 1 — Verificando o estado do repositório

Utilize o comando:

```bash
git status
```

### Perguntas

1. Qual é a finalidade do comando `git status`?
2. O que significa quando o Git informa que não existem alterações para serem commitadas?
3. Qual é a diferença entre um arquivo modificado e um arquivo preparado para commit?

---

## Exercício 2 — Área de preparação

Crie ou altere um arquivo do projeto e execute:

```bash
git status
```

Depois adicione o arquivo à área de preparação:

```bash
git add <arquivo>
```

Execute novamente:

```bash
git status
```

### Perguntas

1. O que mudou após executar `git add`?
2. O arquivo já foi registrado no histórico do Git?
3. Qual comando deve ser utilizado para registrar definitivamente a alteração?

---

## Exercício 3 — Criando um commit

Depois de preparar uma alteração, execute:

```bash
git commit -m "docs: atualiza conteúdo"
```

Depois consulte o histórico:

```bash
git log --oneline
```

### Perguntas

1. O que é um commit?
2. Para que serve a mensagem do commit?
3. Qual informação pode ser obtida utilizando `git log`?

---

## Exercício 4 — Trabalhando com branches

Crie uma nova branch:

```bash
git switch -c feature/teste
```

Confira a branch atual:

```bash
git branch
```

### Perguntas

1. O que é uma branch?
2. Qual é a vantagem de utilizar branches?
3. A branch é uma cópia completa e independente da pasta do projeto?

---

## Exercício 5 — Enviando alterações para o GitHub

Depois de realizar uma alteração e criar um commit, envie a branch para o repositório remoto:

```bash
git push -u origin feature/teste
```

### Perguntas

1. O que o comando `git push` faz?
2. O que significa `origin`?
3. Qual é a finalidade da opção `-u` nesse primeiro envio da branch?

---

## Exercício 6 — Atualizando o repositório

Para buscar alterações existentes no repositório remoto e integrá-las à sua branch, utilize:

```bash
git pull
```

Antes disso, também é possível apenas consultar as alterações remotas utilizando:

```bash
git fetch
```

### Perguntas

1. Qual é a diferença entre `git fetch` e `git pull`?
2. O `git fetch` altera automaticamente os arquivos da sua branch atual?
3. Por que é importante manter o repositório atualizado antes de integrar alterações?

---

## Exercício 7 — Integração de branches

Imagine que uma funcionalidade foi desenvolvida na branch:

```text
feature/teste
```

Para integrá-la à `main`, utilize:

```bash
git switch main
git merge feature/teste
```

### Perguntas

1. Em qual branch o comando `git merge` deve ser executado?
2. O que acontece com as alterações da branch `feature/teste`?
3. O que é um merge fast-forward?

---

## Exercício 8 — Conflitos

Um conflito pode ocorrer quando duas branches possuem alterações incompatíveis na mesma parte de um arquivo.

Durante um conflito, o Git pode apresentar marcadores semelhantes a:

```text
<<<<<<< HEAD
conteúdo da branch atual
=======
conteúdo da outra branch
>>>>>>> feature/teste
```

Para resolver o conflito:

1. Abra o arquivo indicado pelo Git.
2. Escolha ou combine o conteúdo correto.
3. Remova os marcadores de conflito.
4. Salve o arquivo.
5. Execute:

```bash
git add <arquivo>
```

6. Finalize a integração conforme a situação apresentada pelo Git.

### Perguntas

1. Por que um conflito acontece?
2. O Git consegue resolver todos os conflitos automaticamente?
3. Qual é a função dos marcadores `<<<<<<<`, `=======` e `>>>>>>>`?
4. O que deve ser feito depois de resolver manualmente o arquivo?

---

## Exercício 9 — Consultando o histórico

Utilize:

```bash
git log --oneline --graph --decorate --all
```

Observe a representação das branches e dos commits.

### Perguntas

1. O que o comando `--oneline` modifica na apresentação do histórico?
2. Para que serve `--graph`?
3. O que pode ser observado utilizando `--all`?
4. Como o histórico ajuda a entender a evolução de um projeto?

---

## Desafio final

Crie uma pequena alteração no projeto e realize o seguinte fluxo:

```text
Criar/alterar arquivo
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
```

Ao terminar, consulte o histórico utilizando:

```bash
git log --oneline --graph --decorate --all
```

### Objetivo do desafio

Ao concluir o desafio, o estudante deverá demonstrar que consegue:

* verificar o estado do repositório;
* preparar alterações;
* criar commits;
* trabalhar com branches;
* enviar alterações para o GitHub;
* compreender a função do Pull Request;
* integrar alterações;
* consultar o histórico do projeto.

## Resumo

Os exercícios deste módulo permitem praticar o fluxo básico de trabalho com Git e GitHub:

**Alterar → `git add` → `git commit` → `git push` → Pull Request → revisão → merge**

A prática desses comandos ajuda a compreender como o controle de versão pode ser utilizado durante o desenvolvimento de projetos.
