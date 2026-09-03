# 📚 API de Livros

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![Projeto Acadêmico](https://img.shields.io/badge/projeto-acadêmico-blue)
![API REST](https://img.shields.io/badge/API-REST-green)

## 👨‍💻 Sobre o Projeto

Este projeto consiste no desenvolvimento de uma **API REST para gerenciamento de livros**, criada como atividade acadêmica na disciplina de **Sistemas Web II - Grupo B**, da **ETEC Maria Cristina Medeiros**.

A API foi desenvolvida com o objetivo de aplicar, na prática, conceitos relacionados ao desenvolvimento de sistemas web, comunicação entre cliente e servidor e implementação de operações **CRUD** (*Create, Read, Update e Delete*).

O projeto permite realizar operações de **consulta, cadastro, atualização e exclusão de livros** por meio de diferentes rotas HTTP.

---

## 🎯 Objetivo

O principal objetivo deste projeto é desenvolver uma API capaz de **gerenciar informações relacionadas a livros**, utilizando diferentes métodos HTTP para manipulação dos dados.

A aplicação foi estruturada seguindo os princípios de uma **API REST**, permitindo que aplicações externas possam realizar requisições para consultar e modificar os dados disponibilizados pelo sistema.

### Principais objetivos

* 📖 Cadastrar novos livros;
* 🔎 Consultar todos os livros;
* 🔍 Buscar um livro específico pelo ID;
* ✏️ Atualizar informações de um livro;
* 🗑️ Excluir livros;
* 🌐 Aplicar conceitos de APIs REST;
* 💻 Praticar desenvolvimento de sistemas web.

---

## 🔄 Operações da API

A API possui **5 operações principais**, utilizando diferentes métodos HTTP:

| Método   | Rota           | Função                      |
| -------- | -------------- | --------------------------- |
| `GET`    | `/livros`      | Retorna todos os livros     |
| `GET`    | `/livros/{id}` | Retorna um livro específico |
| `POST`   | `/livros`      | Cadastra um novo livro      |
| `PUT`    | `/livros/{id}` | Atualiza um livro existente |
| `DELETE` | `/livros/{id}` | Exclui um livro             |

### 📌 GET — Listar livros

Retorna a lista de livros cadastrados na API.

```http
GET /livros
```

---

### 🔎 GET — Buscar livro por ID

Permite consultar um livro específico utilizando seu identificador.

```http
GET /livros/{id}
```

Exemplo:

```http
GET /livros/1
```

---

### ➕ POST — Cadastrar livro

Utilizado para adicionar um novo livro ao sistema.

```http
POST /livros
```

Exemplo de dados enviados:

```json
{
    "titulo": "Dom Casmurro",
    "autor": "Machado de Assis",
    "ano": 1899
}
```

---

### ✏️ PUT — Atualizar livro

Permite alterar as informações de um livro já cadastrado.

```http
PUT /livros/{id}
```

Exemplo:

```http
PUT /livros/1
```

---

### 🗑️ DELETE — Excluir livro

Remove um livro cadastrado utilizando seu ID.

```http
DELETE /livros/{id}
```

Exemplo:

```http
DELETE /livros/1
```

---

## 🧩 Estrutura CRUD

A API utiliza as quatro operações fundamentais de manipulação de dados:

```text
             📚 API DE LIVROS
                    │
        ┌───────────┴───────────┐
        │                       │
     CONSULTAR                ALTERAR
        │                       │
   ┌────┴────┐              ┌───┴───┐
   │         │              │       │
  GET      GET /ID         POST    PUT
   │         │              │       │
   └────┬────┘              └───┬───┘
        │                       │
        └──────────┬────────────┘
                   │
                DELETE
```

---

## 🛠️ Tecnologias

As tecnologias utilizadas no desenvolvimento do projeto incluem:

* 🌐 **API REST**
* 💻 **Python**
* ⚡ **FastAPI**
* 🗄️ **MySQL**
* 🔗 **SQLAlchemy**
* 📦 **PyMySQL**
* 📄 **JSON**
* 🚀 **Uvicorn**

> *As tecnologias podem ser ajustadas conforme a implementação final do projeto.*

---

## 📂 Estrutura do Projeto

Uma possível organização dos arquivos é:

```text
API-LIVROS/
│
├── 📁 app/
│   ├── main.py
│   ├── database.py
│   ├── models.py
│   ├── schemas.py
│   └── routes.py
│
├── 📄 requirements.txt
├── 📄 README.md
└── 📄 .gitignore
```

A organização pode variar de acordo com a estrutura utilizada durante o desenvolvimento.

---

## 🚀 Como executar o projeto

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/api-livros.git
```

### 2. Acesse a pasta

```bash
cd api-livros
```

### 3. Crie um ambiente virtual

```bash
python -m venv venv
```

### 4. Ative o ambiente virtual

**Windows:**

```bash
venv\Scripts\activate
```

**Linux/macOS:**

```bash
source venv/bin/activate
```

### 5. Instale as dependências

```bash
pip install -r requirements.txt
```

### 6. Execute a API

Caso o arquivo principal seja `main.py`:

```bash
uvicorn main:app --reload
```

A API estará disponível localmente em:

```text
http://127.0.0.1:8000
```

---

## 📖 Documentação da API

Caso esteja utilizando **FastAPI**, a documentação interativa pode ser acessada através de:

### Swagger UI

```text
http://127.0.0.1:8000/docs
```

### ReDoc

```text
http://127.0.0.1:8000/redoc
```

Essas interfaces permitem visualizar as rotas disponíveis e realizar requisições diretamente pelo navegador.

---

## 🧪 Testes das Rotas

As rotas podem ser testadas utilizando ferramentas como:

* Swagger UI;
* Insomnia;
* Postman;
* Thunder Client;
* Navegador, para requisições `GET`.

Exemplo de fluxo:

```text
POST
  ↓
Cadastrar livro
  ↓
GET
  ↓
Consultar livros
  ↓
GET /ID
  ↓
Consultar livro específico
  ↓
PUT
  ↓
Atualizar livro
  ↓
DELETE
  ↓
Excluir livro
```

---

## 🔐 Considerações

Este projeto possui finalidade **acadêmica e educacional**, sendo desenvolvido para colocar em prática conceitos estudados na disciplina de **Sistemas Web II - Grupo B**.

A implementação poderá receber novas funcionalidades futuramente, como autenticação de usuários, validações mais avançadas, paginação, filtros e melhorias na documentação.

---

## 👨‍🎓 Autor

**João Pedro de Andrade Ferreira**

Projeto desenvolvido na:

**ETEC Maria Cristina Medeiros**

Disciplina:

**Sistemas Web II - Grupo B**

Orientação:

**Professor Anderson Vanin**

---

## ⭐ Projeto Acadêmico

Desenvolvido com o objetivo de aplicar conhecimentos de **desenvolvimento web, APIs REST, bancos de dados e operações CRUD** em um projeto prático.

**📚 API de Livros — Sistemas Web II**
