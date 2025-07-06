# 🛠️ CRUD Serverless com AWS (DynamoDB, Lambda, API Gateway e S3)

Este projeto é um exemplo prático de aplicação **serverless** na AWS com operações **CRUD** utilizando:

* **AWS Lambda (Python)** para a lógica de backend
* **Amazon DynamoDB** como banco de dados NoSQL
* **Amazon API Gateway** para expor as rotas HTTP
* **Amazon S3** para hospedar o frontend estático
* **Amazon CloudWatch** para monitoramento e logs

## 🔍 Visão Geral

A aplicação permite **cadastrar, visualizar, atualizar e excluir** produtos de forma simples e rápida. Todas as operações são realizadas através de funções Lambda que interagem com o DynamoDB via API Gateway.

CRUD![tela crud](https://github.com/user-attachments/assets/fbc8c8f2-97fa-4266-a214-4003c5ab0412)
--
Logs Api gateway![logs-api](https://github.com/user-attachments/assets/13b91db6-65dd-4025-bab5-73db036838f4)
--
Logs Api gateway![logs-api](https://github.com/user-attachments/assets/c696d346-cdac-456a-945d-ed20c9083292)

---

## 🧱 Tecnologias Utilizadas

* Python 3.12 (Lambda)
* AWS Lambda
* Amazon DynamoDB
* Amazon API Gateway
* Amazon S3
* Amazon IAM (permissões)
* Amazon CloudWatch

---

## 🚀 Como Executar

> ⚠️ É necessário ter uma conta na AWS com permissões de administrador.

1. **Criar uma Role IAM** com as permissões:

   * `AWSLambdaBasicExecutionRole`
   * `AmazonDynamoDBFullAccess`

2. **Criar uma tabela no DynamoDB** com partição `id (String)`

3. **Criar a função Lambda** e subir o arquivo `CRUD.zip` com o código

4. **Configurar o API Gateway** com rotas para métodos `GET`, `POST`, `PUT`, `DELETE`

5. **Editar o script.js** com o link da API gerado

6. **Criar e configurar o bucket S3** para hospedar os arquivos `index.html`, `style.css` e `script.js`

7. **Habilitar logs no CloudWatch** e configurar CORS no API Gateway

8. **Cadastrar os produtos via interface web** e visualizar a persistência no DynamoDB

---

## 📂 Estrutura de Pastas

```
/frontend
├── index.html
├── style.css
└── script.js

/backend
└── CRUD.py
```

---

## 📸 Exemplo de uso

Cadastrar um produto com:

```json
{
  "id": "1",
  "nome": "Bolsa",
  "preco": 12.50,
  "quantidade": 100
}
```

---

## ✅ Concluído

* [x] CRUD completo via Lambda
* [x] API REST via API Gateway
* [x] Frontend estático no S3
* [x] Logs e monitoramento com CloudWatch

