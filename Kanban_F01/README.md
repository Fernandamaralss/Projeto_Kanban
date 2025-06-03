````markdown
# Kanban 01 – Backend com Express

Este projeto é uma aplicação de gerenciamento de tarefas no estilo **Kanban**, desenvolvida com **Node.js** e **Express**, utilizando armazenamento em memória. Ideal para fins didáticos e projetos iniciais de backend.

---

## ⚙️ Requisitos

- Node.js (versão 14 ou superior)  
- NPM (gerenciador de pacotes)  
- Postman (ou outra ferramenta para testes de API)

---

## 📂 Estrutura do Projeto

```bash
PROJETO_KANBAN
│
├── Kanban_F01
│   ├── node_modules/
│   ├── src/
│   │   └── app.js
│   ├── server.js
│   ├── package-lock.json
│   ├── package.json
│   └── README.md
│
└── README.md
````

---

## 🚀 Rodando o Projeto

### 1️⃣ Clone o repositório

```bash
git clone https://github.com/seu-usuario/KANBAN.V1.git
cd KANBAN.V1
```

### 2️⃣ Instale as dependências

```bash
npm install
```

### 3️⃣ Inicie o servidor

```bash
node src/app.js
```

> ⚠️ **Observação importante:**
> Se estiver utilizando `import` no lugar de `require`, adicione o seguinte no seu `package.json`:
>
> ```json
> {
>   "type": "module"
> }
> ```

O servidor estará disponível em:
`http://localhost:3000`

---

## 🔗 Rotas Disponíveis

### `GET http://localhost:3000/`

* Retorna mensagem de boas-vindas da API

### `GET http://localhost:3000/tarefas`

* Retorna todas as tarefas cadastradas

### `GET http://localhost:3000/tarefas/:id`

* Retorna uma tarefa específica

### `POST http://localhost:3000/tarefas`

* Cria uma nova tarefa

Exemplo de corpo (JSON):

```json
{
  "id": 5,
  "titulo": "Teste Json",
  "descricao": "Serve para testar o POST e o PUT",
  "status": "TO_DO",
  "quadroId": 101
}
```

### `PUT http://localhost:3000/tarefas/:id`

* Atualiza uma tarefa existente

### `DELETE http://localhost:3000/tarefas/:id`

* Remove uma tarefa pelo ID

---

## 🧪 Testando no Postman

1. Abra o Postman
2. Configure a URL: `http://localhost:3000/tarefas`
3. Selecione o método desejado: `GET`, `POST`, `PUT` ou `DELETE`
4. Para `POST` e `PUT`, vá em **Body > raw > JSON**
5. Utilize o JSON de exemplo fornecido acima

---

## ⚠️ Observações

* Os dados são armazenados apenas em memória (não persistem após reinício do servidor).
* Ideal para prática com **Express** e **APIs REST**.

---

Desenvolvido por **Fernanda Amaral Santos** 👩‍💻