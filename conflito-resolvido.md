# Conflito resolvido

## Objetivo

Durante o desenvolvimento do projeto, foi realizado um conflito controlado para praticar o processo de identificação e resolução de conflitos no Git.

## Como o conflito foi criado

Foi criada uma branch chamada `conflito-teste` a partir da branch `main`.

Na branch `conflito-teste`, foi realizada uma alteração no arquivo `aprendizados.md`:

> O projeto permitiu praticar os principais comandos do Git.

Em seguida, a alteração foi registrada com um commit:

```text
docs: adiciona observação sobre a prática do projeto
```

Depois, retornamos para a branch `main` e realizamos outra alteração no mesmo trecho do arquivo `aprendizados.md`:

> A prática contribuiu para compreender melhor o fluxo de versionamento.

Essa alteração também foi registrada em um commit:

```text
docs: adiciona observação sobre versionamento
```

## Geração do conflito

Ao tentar integrar a branch `conflito-teste` à `main` utilizando o comando:

```bash
git merge conflito-teste
```

o Git identificou alterações diferentes no mesmo trecho do arquivo `aprendizados.md` e informou que ocorreu um conflito.

## Resolução

O arquivo apresentou os marcadores de conflito:

```text
<<<<<<< HEAD
A prática contribuiu para compreender melhor o fluxo de versionamento.
=======
O projeto permitiu praticar os principais comandos do Git.
>>>>>>> conflito-teste
```

As duas informações eram relevantes para o projeto. Por isso, os marcadores foram removidos e as duas frases foram mantidas no arquivo.

Depois da resolução, foi executado:

```bash
git add aprendizados.md
```

Em seguida, foi criado o commit de merge:

```bash
git commit -m "merge: resolve conflito em aprendizados"
```

O commit gerado foi:

```text
aceac98 merge: resolve conflito em aprendizados
```

## Resultado

Após a resolução, o histórico passou a apresentar um merge com duas linhas de desenvolvimento, demonstrando o funcionamento de um conflito real no Git.

O estado final do repositório foi verificado com:

```bash
git status
```

Resultado:

```text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

Isso confirmou que o conflito foi resolvido e que todas as alterações foram registradas e enviadas para o repositório remoto.

## Aprendizado

A atividade demonstrou que conflitos podem ocorrer quando diferentes branches modificam a mesma parte de um arquivo. O Git identifica o conflito, mas a decisão sobre qual conteúdo manter ou combinar precisa ser feita pelo desenvolvedor.

A prática também mostrou a importância de verificar o histórico, revisar os arquivos após a resolução e realizar um novo commit para registrar o resultado do merge.
