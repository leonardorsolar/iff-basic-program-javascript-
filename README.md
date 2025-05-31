# Tutorial para Iniciantes — Como rodar e entender o projeto básico de JavaScript e MVC no Node.js

---

## 1. Pré-requisitos — o que você precisa instalar antes

Antes de começar, você precisa instalar 2 programas no seu computador:

### a) Instalar o Git

-   O Git é o programa que permite baixar (clonar) o projeto do GitHub para seu computador.

-   Baixe e instale o Git aqui: [https://git-scm.com/downloads](https://git-scm.com/downloads)

-   Depois de instalar, abra o terminal (Prompt de Comando no Windows, Terminal no Mac/Linux).

-   Para testar se o Git está instalado, digite no terminal:

```bash
git --version
```

Se aparecer um número da versão, está instalado corretamente.

---

### b) Instalar o Node.js

-   O Node.js é a tecnologia que vai permitir executar o código JavaScript no seu computador (fora do navegador).

-   Baixe e instale o Node.js aqui: [https://nodejs.org/](https://nodejs.org/)

-   Depois de instalar, no terminal digite para testar:

```bash
node -v
```

Deve mostrar a versão do Node.js.

---

## 2. Baixando o projeto do GitHub

Agora vamos baixar o seu projeto para o computador.

No terminal, digite:

```bash
git clone https://github.com/leonardorsolar/iff-basic-program-javascript-
```

Este comando vai copiar todos os arquivos do seu projeto para uma pasta chamada `iff-basic-program-javascript-` no seu computador.

---

## 3. Entrar na pasta do projeto

Depois que o download terminar, entre na pasta do projeto:

```bash
cd iff-basic-program-javascript-
```

---

## 4. Entendendo o código simples (função em 01Function)

No arquivo `01Function/function.js` (ou o arquivo que contém o código):

```js
function usuario(nome) {
    return nome
}

let primeiroNome = "leonardo"

const output = usuario(primeiroNome)

console.log(output)
```

### O que esse código faz?

-   Cria uma função chamada `usuario` que recebe um nome e retorna esse nome.
-   Cria uma variável `primeiroNome` com o valor "leonardo".
-   Chama a função `usuario` com esse nome e salva o resultado em `output`.
-   Imprime no console (tela do terminal) o valor do output, que será `"leonardo"`.

---

## 5. Rodando o código simples no terminal

Você pode rodar o código com o Node.js para ver o resultado no terminal.

Digite no terminal:

```bash
node 01Function/function.js
```

Vai aparecer no terminal:

```
leonardo
```

---

## 6. Entendendo o projeto MVC (na pasta 02mvc)

Este projeto está dividido em arquivos que simulam uma aplicação com a arquitetura MVC:

-   **app.js**: é o "ponto de partida" do programa, chama o controller.
-   **controller.js**: processa os dados que chegam e chama o service.
-   **service.js**: lógica principal da aplicação, chama o banco de dados.
-   **database.js**: simula um banco de dados, retorna dados.

---

### Como funciona?

-   O `app.js` cria dados (`{ name: "leonardo" }`) e chama o controller.
-   O `controller.js` recebe esses dados e chama o service.
-   O `service.js` pede os dados para o `database.js`.
-   O `database.js` retorna os dados simulados do banco.
-   O resultado volta pelo caminho inverso e é mostrado no console.

---

## 7. Rodando o projeto MVC

No terminal, dentro da pasta `02mvc`, rode o comando:

```bash
node app.js
```

Você verá no terminal mensagens como:

```
App: Iniciado a função

main ->>

Controller->>

Service ->>

Resposta (retorno da função) para o front

Resposta: id:1 name:leonardo email:leonardo@gmail.com
```

Isso mostra que o fluxo funcionou, passando dados entre as camadas.

---

## 8. Próximos passos para estudar

-   Entender funções, variáveis e objetos em JavaScript.
-   Estudar o que são **módulos** e como importar/exportar funções em arquivos diferentes (`require` e `module.exports`).
-   Aprender como o Node.js executa código JavaScript fora do navegador.
-   Explorar a arquitetura MVC (Model-View-Controller) para organizar seu código.

---

## 9. Resumo dos comandos básicos usados

```bash
git clone https://github.com/leonardorsolar/iff-basic-program-javascript-
cd iff-basic-program-javascript-

# Rodar código simples
node 01Function/function.js

# Entrar na pasta MVC e rodar app.js
cd 02mvc
node app.js
```

---

## 10. Dica final

-   Sempre abra o terminal dentro da pasta certa.
-   Para abrir uma pasta no terminal, clique com o botão direito na pasta e escolha "Abrir no terminal" (se o sistema permitir).
-   Edite os arquivos com o VSCode (Visual Studio Code), que é um editor muito usado para programar.
