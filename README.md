# 🐾 API Pets

API REST desenvolvida com **Node.js e Express** para o gerenciamento de Pets, permitindo cadastrar, consultar, atualizar e excluir registros.

O projeto foi desenvolvido com o objetivo de praticar a criação de APIs REST, o gerenciamento de rotas HTTP, a utilização de métodos CRUD e a manipulação de dados.

## 🛠️ Tecnologias utilizadas

* Node.js
* Express
* JavaScript
* Postman (para testes das rotas)

## 📋 Funcionalidades

* Listar todos os Pets.
* Filtrar Pets por espécie.
* Cadastrar um novo Pet.
* Buscar um Pet pelo ID.
* Atualizar os dados de um Pet.
* Atualizar informações específicas de um Pet.
* Excluir um Pet.

## ⚙️ Como executar o projeto

### Instalação

1. Clone o repositório:

```bash
git clone https://github.com/talitafranciskievicz/API-PETS.git
```

2. Acesse a pasta do projeto:

```bash
cd API-PETS
```

3. Instale as dependências:

```bash
npm install
```

4. Inicie o servidor:

```bash
npm run dev
```

> **Observação:** O comando `npm run dev` depende de estar configurado no `package.json`. Caso não esteja, utilize o comando correspondente à configuração do projeto.

Por padrão, os exemplos abaixo utilizam:

```text
http://localhost:3000
```

## 📌 Endpoints

| Método | Rota        | Descrição                        |
| ------ | ----------- | -------------------------------- |
| GET    | `/pets`     | Lista todos os Pets              |
| POST   | `/pets`     | Cadastra um novo Pet             |
| GET    | `/pets/:id` | Busca um Pet pelo ID             |
| PUT    | `/pets/:id` | Atualiza os dados de um Pet      |
| PATCH  | `/pets/:id` | Atualiza informações específicas |
| DELETE | `/pets/:id` | Exclui um Pet                    |

## 🔍 Exemplos de requisições

### 1. Listar Pets

```http
GET /pets
```

Retorna a lista de Pets cadastrados.

**Filtrar por espécie:**

```http
GET /pets?especie=cachorro
```

Retorna os Pets que correspondem à espécie informada.

### 2. Criar um novo Pet

```http
POST /pets
```

**Body (JSON):**

```json
{
  "nome": "Thor",
  "especie": "cachorro",
  "idade": 3,
  "raca": "Golden Retriever"
}
```

**Campos:**

| Campo     | Tipo   | Obrigatório |
| --------- | ------ | ----------- |
| `nome`    | String | Sim         |
| `especie` | String | Sim         |
| `idade`   | Number | Sim         |
| `raca`    | String | Não         |

### 3. Buscar Pet pelo ID

```http
GET /pets/:id
```

**Exemplo:**

```http
GET /pets/84584ae8-3ce3-4839-99d8-930a34ca3b85
```

Retorna os dados do Pet correspondente ao ID informado.

### 4. Atualizar um Pet

```http
PUT /pets/:id
```

**Body (JSON):**

```json
{
  "nome": "Thor",
  "especie": "cachorro",
  "idade": 4,
  "raca": "Golden Retriever"
}
```

Atualiza os dados do Pet identificado pelo ID.

### 5. Atualizar informações específicas

```http
PATCH /pets/:id
```

Atualiza uma informação específica de um Pet.

**Exemplo:**

```json
{
  "idade": 4
}
```

### 6. Excluir um Pet

```http
DELETE /pets/:id
```

Exclui o Pet correspondente ao ID informado.

## 🧪 Testes

As requisições podem ser testadas utilizando o **Postman**.

📄 **Documentação completa:** https://documenter.getpostman.com/view/56936131/2sBYB4K6RE.
