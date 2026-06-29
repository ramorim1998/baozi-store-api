# Baozi Store API

API REST desenvolvida em Java com Spring Boot para gerenciamento de clientes, produtos e pedidos de uma loja de pães chineses.

## Tecnologias

* Java 21
* Spring Boot 4.1.0
* Spring Data JPA
* H2 Database
* Lombok
* Maven

## Como executar

### Clone o repositório

```bash
git clone https://github.com/seu-usuario/baozi-store-api.git
cd baozi-store-api
```

### Execute a aplicação

No VS Code, abra a classe `BaoziStoreApiApplication.java` e clique em **Run**.

Ou execute pelo terminal:

**Linux/macOS**

```bash
./mvnw spring-boot:run
```

**Windows**

```bash
mvnw.cmd spring-boot:run
```

A aplicação ficará disponível em:

```
http://localhost:8080
```

## Endpoints

### Clientes

| Método | Endpoint         |
| ------ | ---------------- |
| POST   | `/clientes`      |
| GET    | `/clientes`      |
| GET    | `/clientes/{id}` |
| DELETE | `/clientes/{id}` |

### Produtos

| Método | Endpoint         |
| ------ | ---------------- |
| POST   | `/produtos`      |
| GET    | `/produtos`      |
| GET    | `/produtos/{id}` |
| DELETE | `/produtos/{id}` |

### Pedidos

| Método | Endpoint        |
| ------ | --------------- |
| POST   | `/pedidos`      |
| GET    | `/pedidos`      |
| GET    | `/pedidos/{id}` |
| DELETE | `/pedidos/{id}` |

## Exemplos de requisições

### Cadastrar cliente

```http
POST /clientes
```

```json
{
  "nome": "Rafael Araujo Amorim - RU 4327268",
  "clienteDesde": "2026-06-15"
}
```

### Cadastrar produto

```http
POST /produtos
```

```json
{
  "nome": "Pão Chinês Tradicional",
  "preco": 12.50,
  "estoque": true
}
```

### Cadastrar pedido

```http
POST /pedidos
```

```json
{
  "clienteId": 1,
  "produtoId": 1,
  "quantidade": 8
}
```

## Banco de dados

O projeto utiliza o H2 Database em memória para armazenamento dos dados durante a execução da aplicação.

## Autor

Rafael Araujo Amorim
RU 4327268

Desenvolvimento Web Back-End - UNINTER
