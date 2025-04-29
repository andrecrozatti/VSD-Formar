# 🧠 Aula 1 - Introdução ao Backend com Node.js + TypeScript

Bem-vindo à primeira aula do nosso curso de backend!  
Hoje vamos aprender o que é backend, entender os conceitos principais do desenvolvimento de APIs, configurar seu ambiente e criar o seu primeiro projeto com Node.js + TypeScript.

---

## 📌 O que vamos ver hoje

- O que é backend?
- O que é API e API REST?
- O que são HTTP Methods?
- O que é um framework?
- O que é ORM?
- O que é Node.js e TypeScript?
- Como configurar o ambiente
- Como instalar o Node.js e o npm
- Como criar seu primeiro projeto backend com Node.js + TS

---

## 💡 O que é Backend?

O **backend** é a parte do sistema que roda “por trás dos panos”.

É responsável por:
- Processar regras de negócio
- Armazenar e consultar dados em um banco de dados
- Enviar dados para o frontend (a interface que o usuário vê)

📦 Exemplo: Quando você acessa o iFood, o frontend mostra os restaurantes, mas é o **backend** que busca essas informações no banco de dados.

---

## 🔌 O que é uma API?

API significa **Application Programming Interface**, ou **Interface de Programação de Aplicações**.

Ela permite que dois sistemas se comuniquem.  
No nosso caso, a API vai permitir que o frontend (site ou app) se comunique com o backend.

📬 **Exemplo prático**: Quando você entra no Instagram, o app chama a API para buscar as fotos, comentários, curtidas, etc.

---

## 🌐 O que é uma API REST?

REST é um estilo de arquitetura de APIs.  
Uma **API REST** utiliza o protocolo HTTP (aquele das páginas web) para enviar e receber dados, geralmente em **JSON**.

Ela organiza os dados em **recursos**. Por exemplo:
- `/users` representa os usuários
- `/products` representa os produtos

---

## 🧭 O que são HTTP Methods?

São os "verbos" que usamos para indicar a ação que queremos fazer com os dados da API.

| Método | Ação | Exemplo               |
|--------|------|------------------------|
| GET    | Ler  | `GET /users`           |
| POST   | Criar| `POST /users`          |
| PUT    | Atualizar tudo | `PUT /users/1` |
| PATCH  | Atualizar parcial | `PATCH /users/1` |
| DELETE | Apagar | `DELETE /users/1`    |

---

## 🧱 O que é um Framework?

Um **framework** é um conjunto de ferramentas que facilita o desenvolvimento.

No backend com Node.js, o framework mais usado é o **Express**, que ajuda a criar servidores e rotas de forma rápida e simples.

---

## 🔄 O que é um ORM?

ORM significa **Object-Relational Mapping**.

Ele traduz os dados do banco de dados (linhas e tabelas) em objetos no seu código.

Vamos usar o **Prisma ORM**, que permite:
- Criar tabelas com código
- Escrever consultas no banco com TypeScript
- Validar e modelar dados de forma fácil

---

## ⚙️ O que é Node.js?

Node.js é um ambiente para rodar JavaScript fora do navegador.  
É ideal para criar aplicações modernas, como APIs, bots e sistemas em tempo real.

---

## 🔤 O que é TypeScript?

TypeScript é uma versão melhorada do JavaScript. Ele adiciona **tipos**, como `string`, `number`, etc.

✅ Isso evita erros e melhora a produtividade do desenvolvedor.

---

## 🛠️ Como instalar o Node.js + npm

### 1. Baixe o Node.js

Acesse: [https://nodejs.org/](https://nodejs.org/)

Baixe a versão **LTS** (a mais estável).  
Ao instalar o Node, o **npm** já vem junto automaticamente.

---

## 📦 O que é o npm?

O `npm` (Node Package Manager) é o gerenciador de pacotes do Node.js.  
Ele permite instalar bibliotecas e ferramentas no seu projeto.

---

## 🚀 Criando seu primeiro projeto Node.js + TS

### Passo 1: Criar uma nova pasta e abrir no VSCode
```bash
mkdir meu-primeiro-backend
cd meu-primeiro-backend
code .
```
### Passo 2: Executar o comando init para iniciar um projeto node
```bash
npm init -y
```

### Passo 3: Instalar o Typescript ao projeto
```bash
npm install typescript ts-node-dev @types/node -D
```
- typescript: compilador TS

- ts-node-dev: executa arquivos .ts sem precisar compilar

- @types/node: permite que o TypeScript entenda funções do Node

### Passo 4: Inicar o typescript
```bash
npx tsc --init
```
- Isso fará com que o arquivo tsconfig.json seja criado


### Passo 5: Editar o arquivo *package.json*
```JSON
"scripts": {
    "start": "tsc && ts-node src/index.ts"
}
```
### Passo 6: Criar a pasta src na raiz do projeto e o arquivo index.ts dentro da mesma
- ./src/index.ts
- Dentro do arquivo acrescentar o código abaixo:
    ```JavaScript
    console.log('Servidor rodando com Node.js e TypeScript!');
    ```
### Passo 7: Executar o comando abaixo para iniciar o projeto
```bash
    npm start
```
