# Fortics-test-API

Uma API simples para manipulação de comentários, construída com **Node.js** e **SQLite**.

## 📋 Funcionalidades
- **GET `/`**: Retorna todos os comentários armazenados no banco de dados.
- **POST `/`**: Adiciona um novo comentário, validando o tamanho do texto.

## 🚀 Tecnologias Utilizadas
- **Node.js**: Para o servidor e a lógica de negócios.
- **Express.js**: Framework para gerenciamento de rotas.
- **SQLite**: Banco de dados leve e eficiente.

## 📂 Estrutura do Projeto
```
Fortics-test-API/
├── src/
│   ├── database/
│   │   ├── tables/
│   │   │   └── comments.js
│   │   ├── database.js
│   │   └── twitter.db
├── .gitignore
├── README.md
├── index.js
├── package-lock.json
├── package.json
└── tailwind.config.js
```

## 🛠️ Como Configurar e Executar

### 1. Clone o Repositório
```bash
git clone https://github.com/LeoSilva91/Fortics-test-API.git
cd Fortics-test-API
```

### 2. Instale as Dependências
```bash
npm install
```

### 3. Execute a API
```bash
node index.js
```

Acesse a API localmente em [http://localhost:3000](http://localhost:3000).

---

## 📝 Rotas

### **GET `/`**
Retorna a lista de comentários ordenados pela data (mais recentes primeiro).

**Exemplo de Resposta:**
```json
[
  {
    "id": 1,
    "name": "Leonardo",
    "comment": "API funcional e bem estruturada.",
    "date": "2025-01-09"
  }
]
```

### **POST `/`**
Adiciona um novo comentário.

**Parâmetros no Body (JSON):**
- `name` (string): Nome do autor do comentário.
- `comment` (string): Texto do comentário (mínimo 10 caracteres, máximo 145).
- `date` (string): Data no formato ISO.

**Exemplo de Body:**
```json
{
  "name": "Leonardo",
  "comment": "Este é um teste.",
  "date": "2025-01-09"
}
```

**Resposta de Sucesso:**
```json
{
  "id": 2,
  "name": "Leonardo",
  "comment": "Este é um teste.",
  "date": "2025-01-09"
}
```

---

## 🔧 Melhorias Futuras
- Implementar autenticação para acesso às rotas.
- Adicionar testes automatizados.
- Expandir a API com mais endpoints.
- Otimizar mensagens de erro e validações.

---

## 🤝 Contribuições
Contribuições são bem-vindas! Siga os passos:
1. Faça um fork do projeto.
2. Crie uma branch para sua modificação: `git checkout -b minha-modificacao`.
3. Faça o commit: `git commit -m 'Descrição da alteração'`.
4. Faça o push: `git push origin minha-modificacao`.
5. Abra um Pull Request.

---

## 📝 Licença
Este projeto está sob a licença MIT. Use, modifique e distribua à vontade! 😊

--- 
